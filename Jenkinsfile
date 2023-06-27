node{
    def maven= tool name:"maven3.9.2"
    stage('GIT CHECKOUT')
    {
        git credentialsId: 'bbacb9bc-823f-4fc0-af56-7cd9a2a50f98', url: 'https://github.com/KmnsKns/kns.git'
    }
    stage('BUILD')
    {
        sh "$maven/bin/mvn clean package"
    }
    stage('SONAR REPORT')
    {
        sh "$maven/bin/mvn sonar:sonar"
    }
}
