pipeline{
    agent any
    stages{
        stage("checkout"){
            steps{
                checkout([$class: 'GitSCM',
                branches: [[name: '*/master']],
                extensions: [],
                userRemoteConfigs: [
                                    [credentialsId: 'Ravitezzzz45',
                                     url: 'https://github.com/Ravitezzzz45/webapplication']]
                                    ])
            }
        }
        stage("test"){
            steps{
                echo "this is tested"
            }
        }
         stage("QA"){
            steps{
                echo "this is tested"
            }
        }
      stage("build"){
            steps{
                echo "this is tested"
            }
        }  
        stage("artifactory push"){
            steps{
                echo "this is tested"
            }
        }  
        stage("create image"){
            steps{
                echo "this is tested"
            }
        }  
        stage("deploy to k"){
            steps{
                echo "this is tested"
            }
        }  
    }
    post{
        success{
            echo "this is post"
        }
    }
}