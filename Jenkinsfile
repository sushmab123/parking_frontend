pipeline {
 agent any
     stages {
      stage('Build') {
         steps {
            // Get code from a GitHub repository
            git 'https://github.com/sushmab123/parking_frontend.git'

            // Run npm on a Unix agent.
				sh 'npm install'
				sh 'npm run build'

                }

       
                    }
	 stage('Deploy') 
	 {
         steps {
            // deploy to tomcat
			sh 'cd $WORKSPACE;chmod 777 build;cp -r build /opt/apache-tomcat-9.0.27/webapps'
            
                }
     }
            }
}
