#!/bin/bash -l

pipeline {
  agent any
  tools {nodejs "latest"}
  stages {
    stage('Pre-checks 2') {
      steps {
        sh 'node -v'
      }
    }
    stage('Build from Master 2') {
      steps {
        sh 'git log --reverse -1'
        sh 'npm install'
      }
    }
    stage('Start Test') {
      steps {
        sh 'npm test'
      }
    }
    stage('Start App') {
      steps {
        sh 'npm start'
      }
    }
  }
}
