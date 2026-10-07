pipeline {
    agent {
        node {
            label "linux && java11"
        }
    }

    stages {
        stage("hello") {
            steps {

            echo ("Hello World")
            }
        }

         stage("build"){
             steps{
                echo("Start build")
                sh("./mvmw clean compile test-compile")
                echo("End build")
            }
        } 
        stage("test"){
            steps{
                echo("Start test")
                sh("./mvmw clean compile test-compile")
                echo("End test")
            }
        }
        stage("deploy"){
            steps{
                echo("ini test")
            }
        }
    }

    post{
        always{
            echo "====++++always++++===="
        }
        success{
            echo "====++++only when successful++++===="
        }
        failure{
            echo "====++++only when failed++++===="
        }
        cleanup{
            echo "====++++something++++===="
        }
    }
}