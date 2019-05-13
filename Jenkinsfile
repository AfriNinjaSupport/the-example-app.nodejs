#!/bin/bash -l

pipeline {
  agent any
  tools {nodejs "latest"}
  stages {
    stage('Pre-checks 2') {
      steps {
        echo sh(returnStdout: true, script: 'env')
        sh 'node -v'
      }
    }
    stage('Build from Master 2') {
      steps {
        sh 'npm --version'
        sh 'git log --reverse -1'
        sh 'npm install'
      }
    }
    stage('Start Test') {
      steps {
        sh 'npm test'
      }
    }
  }
}
