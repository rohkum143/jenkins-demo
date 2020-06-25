pipeline {
  agent {
    kubernetes {
      yaml """
apiVersion: v1
kind: Pod
metadata:
  labels:
    some-label: test
spec:
  containers:
  - name: jnlp
    image: jenkinsci/jnlp-slave
    command:
    - cat
    tty: true
"""
    }
  }
  stages {
    stage('test') {
      steps {
        echo 'hello world '
      }
    }

  }
}
