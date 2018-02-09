node('master') {
stage 'checkout'
checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'e37d71ea-b094-4ef9-8f90-81d186e2e6dc', url: 'https://github.com/grvdeep/project2.git']]])
stage 'build'
env.DIRPATH=pwd()
sh "echo ${env.DIRPATH}"
env.BRANCH=env.BRANCH_NAME
sh "echo ${env.BRANCH}"
sh """cd ${env.DIRPATH}/example 
mvn clean package"""
}


