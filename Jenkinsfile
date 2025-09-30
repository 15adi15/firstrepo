pipeline {
    agent any

    triggers {
        cron('H/15 * * * *')
    }

    stages {
        stage('Build and Run') {
            steps {
                script {
                    echo '--- Compiling with Full Path ---'

                    // Use bat for Windows
                    // The quotes are important!
                    bat '"C:\\Program Files\\Java\\jdk-21\\bin\\javac.exe" HelloWorld.java'

                    echo '--- Listing Files ---'
                    bat 'dir'

                    echo '--- Running with Full Path ---'
                    bat '"C:\\Program Files\\Java\\jdk-21\\bin\\java.exe" HelloWorld'
                }
            }
        }
    }
}