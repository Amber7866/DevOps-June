pipeline {
         agent any
         stages {
                 stage('One') {
                 steps {
                     echo 'Hi, this is bhagi/Amber from edureka and welcome you to SRE/DevOps 2023 classes'
                 }
                 }
                 stage('Two') {
                 steps {
                    input('Do you want to proceed?')
                 }
                 }
                 stage('Three') {
                 when {
                       not {
                            branch "master"
                       }
                 }
                 steps {
                       echo "Hello"
                 }
                 }
             
}
}
