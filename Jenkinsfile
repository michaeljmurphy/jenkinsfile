#!/usr/bin/env groovy

podTemplate(label: 'mypod', containers: [
    containerTemplate(name: 'sfdx', image: 'mjmsfdc/sfdx', ttyEnabled: true, command: 'cat'),
  ],
  volumes: [
    hostPathVolume(mountPath: '/var/run/docker.sock', hostPath: '/var/run/docker.sock'),
  ]
  ) {
    node('mypod') {
        stage('build') {
            container('sfdx') {
                sh 'sfdx --help'
            }
        }
        
        stage('test') {
            container('sfdx') {
                sh 'sfdx --help'
            }
        }

        stage('dataload') {
            container('sfdx') {
                sh 'sfdx --help'
            }
        }
    }
}
