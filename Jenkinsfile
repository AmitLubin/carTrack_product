pipeline {
    agent any

    options {
        timestamps()
        timeout(time: 20, unit: 'MINUTES')
    }

    environment {
        MVN="mvn -s settings.xml"
    }

    stages {
        stage('Git-checkout'){
            when {
                branch 'release/*'
            }

            steps {
                deleteDir()
                checkout scm
            }
        }
    }
}