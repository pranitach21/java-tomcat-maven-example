pipeline {
  agent any 
          tools { maven “MAVEN_HOME” }
          stages {
                  stage ( ‘Git’ )
                        {
                         steps {
                                git branch : master,
                                credentialsId: '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'
                                url: 'https://github.com/pranitach21/java-tomcat-maven-example.git '
                                  }
                        }
                 stage ( 'Build' )
                       {
                         steps {
                                sh 'mvn -B -DskipTests clean package'
                              }
                       }
                stage ( 'Deploy’)
                      {
                        steps {
                             sh 'cp -ivr /opt/tomcat/.jenkins/workspace/project_java_16/target/udit.war  /opt/tomcat/webapps'
                             }
                      }
          }
  
}
