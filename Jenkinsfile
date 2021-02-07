node {
    def jsonObj = readJSON file: 'Parameter.json'
    def build_tag_one = (jsonObj['is_rollback'] &&  !jsonObj['is_release']) ? jsonObj.Rollback : jsonObj.Release
    stage('Test') {
      parallel payout: {
        dir ('payout-db-util/current') {
          git(branch: 'main',url: 'https://github.com/sankalp92/Jenkins_Pipeline_CICD.git')
        }
      },
      servicestarterkit: {
        dir ('servicestarterkit/current') {
          git(branch: 'main',url: 'https://github.com/sankalp92/Jenkins_Pipeline_CICD.git')
        }
      }
    }
}
