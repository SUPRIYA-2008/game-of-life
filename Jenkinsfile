pipeline {
    agent { label 'JDK-8'}
    triggers {
        pollSCM('* * * * * ')
    }
    tools {
       maven 'mvn 3.6' 
       jdk 'jdk-8'
    }
    stages { 
        stage('git') {
            steps {
                 git url: 'https://github.com/SUPRIYA-2008/game-of-life.git',
                     branch: 'master'
            }
        }
        stage('build and package') {
            steps { 
               sh script : 'mvn clean package'
            }
        }       
    }
}    
