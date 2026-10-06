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