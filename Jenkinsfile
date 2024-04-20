pipeline
{
agent any
stages
{
 stage('scm checkout: download code from github')
 {steps { git branch: 'master', url: 'https://github.com/prakashk0301/mavenproject'  }}

 stage ('execute unit test framework')
 {steps {withMaven(globalMavenSettingsConfig: '', jdk: 'JAVA-HOME', maven: 'MAVEN-HOME', mavenSettingsConfig: '', traceability: true)
   sh 'mvn test'
    }}

 }
}
