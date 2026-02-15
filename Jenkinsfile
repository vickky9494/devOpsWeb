pipeline{

agent any 
   
    stage('clone'){
steps{
        git branch: 'feature/2026.02.11', credentialsId: 'vickky9494', url: 'https://github.com/vickky9494/devOpsWeb.git'
    }
}
    stage('Build'){
steps{
        bat 'mvn clean install'
    }
}
    stage('Test'){
steps{
        bat "mvn test"
    }
}
   stage('Generative Junit Tests result'){
  steps{
        junit 'target/surefire-reports/*.xml'
    }
}
    stage('published Artifacts'){
        archiveArtifacts artifacts: 'target/*.war', followSymlinks: false
    }
}