pipeline
{
agent any
stages
{
 stage('scm checkout: download code from github')
 {steps { git branch: 'master', url: 'https://github.com/ARUNMAHANWAR/mavenproject'  }}


 stage('execute unit test framework')
 {steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JAVA_HOME', maven: 'MAVEN_HOME', mavenSettingsConfig: '', traceability: true) {
    sh 'mvn test'
} } }


 stage('generate artifact')
 {steps { withMaven(globalMavenSettingsConfig: '', jdk: 'JAVA_HOME', maven: 'MAVEN_HOME', mavenSettingsConfig: '', traceability: true) {
    sh 'mvn package'
} } }
  

}

}
