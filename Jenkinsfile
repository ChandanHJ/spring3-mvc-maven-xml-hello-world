node {
   def mvnHome
      stage('getscm') { // for display purposes
            // Get some code from a GitHub repository
	          git 'https://github.com/ChandanHJ/spring3-mvc-maven-xml-hello-world.git'
		        // Get the Maven tool.
			      // ** NOTE: This 'M3' Maven tool must be configured
			            // **       in the global configuration.           
				          mvnHome = tool 'Maven'
					     }
					        stage('Build') {
						      // Run the maven build
						            if (isUnix()) {
							             sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean package"
								           } else {
									         echo 'this is build maven artifact'
										          bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
											        }
												   } 
												      stage ('deploy'){
												         echo 'deployment started'
 													        bat '''copy C:\\Users\\Administrator\\.jenkins\\workspace\\Pipeline_Deployment\\       target\\*.war E:\\Madhu_Devops\\Madhu_softwares\\apache-tomcat-9.0.27-windows-x64\\apache-tomcat-9.0.27\\webapps\\'''
														   }
														      
														      }

