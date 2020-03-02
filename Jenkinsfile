#!/usr/bin/env groovy
import hudson.model.*
import hudson.EnvVars
import java.net.URL

node{
    stage('Git Checkout'){
        git 'https://github.com/gianchandanijeetendra/DevOpsClassCodes.git'
    }
    stage('Compile Addressbook'){
        withMaven(maven:'MyMaven'){
            sh 'mvn compile'
        }
    }
    stage('Package Addressbook'){
        withMaven(maven:'MyMaven'){
            sh 'mvn package'
        }
    }
}
