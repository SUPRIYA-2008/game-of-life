pipeline {
    agent { label 'JDK-8'}
    triggers {
        pollSCM('* * * * * ')
    }
    tools {
       maven 'mvn 3.6', 
       jdk 'jdk-8' 
    }
    stages { 
        stage('git') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/SUPRIYA-2008/game-of-life.git'
            }
        }
        stage('build and package') {
            steps { 
               sh script : 'mvn package'
            }
        }       
    }
}    
