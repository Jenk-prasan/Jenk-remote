pipeline{
    agent none
    options{
        buildDiscarder(logRotator(numToKeepStr:'5'))
    }
  environment {
      Ad = "/home/jenkins/dt"
  }
   stages{
       stage ('Remote ssh'){
           agent {label 'ssh'}
           steps {
               script {

                   sh 'hostname'
                   sh 'rm -rf ${Ad}'
                   sh 'mkdir -p ${Ad}'
                   sh 'ls -l ${Ad}'

               }
           }

       }

   }
}
