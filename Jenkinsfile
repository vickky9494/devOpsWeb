pipeline{

agent any 
   stages{
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
   
    stage('published Artifacts'){
steps{
        archiveArtifacts artifacts: 'target/*.war', followSymlinks: false
}
    }
}
}