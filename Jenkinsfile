def TERRAFORM_REPO = "https://github.com/artak116/jenkins.git"

node(){
  stage("SCM"){
  checkout([$class: 'GitSCM', branches: [[name: "master"]], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'RelativeTargetDirectory', relativeTargetDir: ""]], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/artak116/jenkins.git']]])
  load 'vars/aws.groovy'
  }

  stage("tf plan"){
    print "planing"
    print BB
    sleep 15
  }

  // stage('Verify') {
  //       def userInput = input(
  //           id: 'userInput', message: 'This is PRODUCTION!', parameters: [
  //           [$class: 'BooleanParameterDefinition', defaultValue: false, description: '', name: 'Please confirm you sure to proceed']
  //       ])
  //
  //       if(!userInput) {
  //           error "Build wasn't confirmed"
  //       }
  //   }

  stage("tf apply"){
  print "applying"
  }
}
