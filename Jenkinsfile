node('master') {
stage 'checkout'
checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '5c5bf556-738a-4c78-86c2-c6d8158e52f9', url: 'https://github.com/grvdeep/project2.git']]])
stage 'build'
env.DIRPATH=pwd()
sh "echo ${env.DIRPATH}"
env.BRANCH=env.BRANCH_NAME
sh "echo ${env.BRANCH}"
sh """cd ${env.DIRPATH}/example 
mvn clean package"""
}


