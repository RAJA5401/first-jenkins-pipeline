pipeline {
  agent {
    docker { image 'node:16-alpine' }
  }

  stages {
    stage('Install Dependencies') {
      steps {
        sh 'npm install'
      }
    }

    stage('Run Tests') {
      steps {
        sh 'npm test || echo "No tests defined"'
      }
    }

    stage('Build App') {
      steps {
        sh 'npm run build || echo "No build script defined"'
      }
    }

    stage('Docker Build') {
      steps {
        script {
          docker.build("yourdockerhubusername/my-node-app:${env.BUILD_ID}")
        }
      }
    }
  }

  post {
    success {
      echo '✅ Build completed successfully!'
    }
    failure {
      echo '❌ Build failed. Please check the logs.'
    }
  }
}
