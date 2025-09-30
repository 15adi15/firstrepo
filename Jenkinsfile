pipeline {
    // 1. Agent: Specifies where the pipeline will run. 'any' means any available agent.
    agent any

    // 2. Triggers: Defines how the pipeline is automatically started.
    // This cron syntax will run the pipeline every 15 minutes[cite: 25, 29].
    triggers {
        cron('H/15 * * * *')
    }

    // 3. Stages: Defines the different stages of the pipeline.
    stages {
        // The "Build" stage
        stage('Build') {
            steps {
                // Steps to execute in the "Build" stage
                script {
                    echo '--- Compiling the Java Code ---'
                    
                    // Use 'bat' for Windows or 'sh' for Linux/macOS
                    if (isUnix()) {
                        sh 'javac HelloWorld.java'
                    } else {
                        bat 'javac HelloWorld.java'
                    }
                    
                    echo '--- Compilation Complete ---'
                }
            }
        }
    }
}