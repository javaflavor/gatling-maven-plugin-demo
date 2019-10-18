#!groovy

node('maven') {
    stage('Checkout Source') {
        checkout scm
    }

    stage("Performance Test") {
        try {
            sh "mvn gatling:test"
        }
        finally {
            gatlingArchive()
        }
    }
}
