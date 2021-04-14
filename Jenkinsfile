pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('One') {
            steps {
                echo 'Hi, this is a test --------234--'
            }
        }

        // stage('Two') {
        //     steps {
        //         input('Do you want to proceed?')
        //     }
        // }

        stage('Deploy') {
            steps {
                sshagent(['Dev1_instance_ssh']) {
                    sh '''
                        ssh -o StrictHostKeyChecking=no ubuntu@34.197.45.248 "
                            ls
                            cd /home/ubuntu/nft-web
                            pwd
                            ls
                        "
                    '''
                }
            }
        }
    }
}
