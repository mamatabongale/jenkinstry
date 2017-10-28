node {
        stage 'SCM Polling'
        git url: "https://github.com/mamatabongale/jenkinstry.git"
        
        stage 'Maven Build'
        sh "/opt/apache-maven-3.5.0/bin/mvn clean install"
        archive 'target/*.war'
        
        stage 'Docker Build'
        def pkg = docker.build ("mamata/trail", '.')
       }
