pipeline 
{

    agent any 
    stages {
        stage('MunitTest Application') { 
        steps {
            bat 'mvn clean test'
                // 
            } 
        }
        stage('Build Application') { 
            steps {
            bat 'mvn clean install'
                // 
            }
        }
        stage('Deploying application To Mulesoft cloudhub') { 
            steps {
            bat 'mvn clean deploy -DmuleDeploy  -Dmule.version=4.4.0 -Danypoint.username=akbar_khan1 -Danypoint.password=Mymulesoft@20 -Denv=Sandbox -Dappname=sys-rawg-api -Dbusiness=cap4 -DvCore=Micro -Dworkers=1'
                // 
            } 
        }
    }
}