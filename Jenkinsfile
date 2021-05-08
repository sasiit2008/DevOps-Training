node {

stage 'checkout'
git 'https://github.com/sasiit2008/DevOps-Training.git'

stage 'sonar Analysis'
sh 'mvn sonar:sonar -Dsonar.projectKey=sasiit2008_DevOps-Training -Dsonar.organization=sasiit2008 -Dsonar.host.url=https://sonarcloud.io

stage 'compile'
sh 'mvn compile'

stage 'test'
sh 'mvn test'

stage 'package'
sh 'mvn package'

stage 'artifacts'
archiveArtifacts 'target/*.war'

}
