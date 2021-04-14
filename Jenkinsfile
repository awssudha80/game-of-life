node('MASTER')
   stage('git') {
       git 'https://github.com/awssudha80/game-of-life.git'
   }
   stage ('build'){
       sh 'mvn clean package'
   }
   stage ('test results'){
       junit 'gameoflife-web/target/surefire-reports/*.xml'
   }
   stage ('archive'){
       archiveArtifacts artifacts: 'gameoflife-web/target/*.war', followSymlinks: false
   }