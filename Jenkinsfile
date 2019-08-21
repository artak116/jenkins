node(){
  stage("SCM"){
  checkout([$class: 'GitSCM', branches: [[name: "${TERRAFORM_BRANCH}"]], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'RelativeTargetDirectory', relativeTargetDir: "${CLUSTER}"]], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/artak116/jenkins.git']]])
  print "hello"
  }
}
