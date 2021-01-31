pipeline {
  agent any
  stages{
        stage('git checkout'){
         parallel {
                stage('clone payout-db-util') {
                    steps {
                       dir ('payout-db-util/current') {
                       git(branch: 'main',url: 'https://github.com/sankalp92/Jenkins_Pipeline_CICD.git')
                      }
                    }
                }
                stage('clone servicestarterkit') {
                    steps {
                       dir ('servicestarterkit/current') {
                       git(branch: 'main',url: 'https://github.com/sankalp92/Jenkins_Pipeline_CICD.git')
                      }
                    }
                }
                stage('clone baseclient') {
                    steps {
                       dir ('baseclient/current') {
                       git(branch: 'main',url: 'https://github.com/sankalp92/Jenkins_Pipeline_CICD.git')
                      }
                    }
                }
         }
        } 
  }
}
