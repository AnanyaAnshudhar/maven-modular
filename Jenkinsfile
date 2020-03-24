pipeline{
    agent any
    stages{
        stage('SCM checkout'){
            steps{
                git 'https://github.com/AnanyaAnshudhar/maven-modular.git'
               
            }
           
        }
        stage('Build'){
            steps{
                sh '/usr/share/maven/bin/mvn clean package -Dmaven.test.skip=true'
            }
        }
   

      stage('release'){
         

            steps{
                sh '/usr/share/maven/bin/mvn --batch-mode release:clean release:prepare release:perform \

       -DreleaseVersion=1.0.0 -DdevelopmentVersion=1.0.1-SNAPSHOT`
            }
        }
       
     
    }
}
