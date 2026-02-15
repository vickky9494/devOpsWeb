node{
    
    stage('clone'){
        git branch: 'feature/2026.02.11', credentialsId: 'vickky9494', url: 'https://github.com/vickky9494/devOpsWeb.git'
    }
    stage('Build'){
        bat 'mvn clean install'
    }
    stage('Test'){
        bat "mvn test"
    }
    stage('generated test results'){
        junit 'target/surefire-reports/*.xml'
    }
    stage('published Artifacts'){
        archiveArtifacts artifacts: 'target/*.war', followSymlinks: false
    }
}