pipeline {
    agent {
        node {
            label 'maven'
        }
    }
    tools {
      mvn 'maven_3.9.2'
    }

    stages {
       stage("build"){
            steps {
                 echo "----------- build started ----------"
                sh 'mvn clean deploy -Dmaven.test.skip=true'
                 echo "----------- build complted ----------"
            }
        }
        stage("test"){
            steps{
                echo "----------- unit test started ----------"
                sh 'mvn surefire-report:report'
                 echo "----------- unit test Complted ----------"
            }

    
    }
}
}