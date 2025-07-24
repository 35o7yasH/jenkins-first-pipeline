# 🚀 Jenkins First Pipeline

This repository contains my **first Jenkins pipeline project**, designed to run a basic Node.js version check using a Docker agent.

---

## 📄 Jenkinsfile Overview

The `Jenkinsfile` defines a simple CI pipeline that:

- Uses a lightweight Node.js Docker image (`node:16-alpine`)
- Runs a shell command to display the Node.js version

### 🔧 Jenkinsfile Code

```groovy
pipeline {
  agent {
    docker { image 'node:16-alpine' }
  }
  stages {
    stage('Test') {
      steps {
        sh 'node --version'
      }
    }
  }
}
