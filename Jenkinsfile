#!/usr/bin/env groovy

node {
    stage('checkout') {
        checkout scm
    }

    stage('check java') {
        sh "java -version"
    }
    
    stage('deploy') {     
        sh "pwd"   
        sh "cp ./target/*.jar /opt/jh-blog/app.jar"
        sh "systemctl restart blog"
    }
}
