# Please find the runnable jar and documentations in the following google drive folder https://drive.google.com/drive/folders/1mE_m2YwL9qukj9bR10u8JXYIItAPf8iz 

# Regarding the deliverables

	# A fully running Java application.
		- Please find the packaged spring boot application "mobile-search-api.jar" in the above google drive location 
		- or please pull the image "ssayed7190/sameh-public-repo:mobile-search-api" from docker hub https://hub.docker.com/r/ssayed7190/sameh-public-repo/tags

	# Source code: sent through email, or uploaded to a Git repository and showing the different commits done throughout the different stages of the assignment.
		- Kindly find the below github "mobile-search-api" repo 
		https://github.com/S-Sayed/mobile-search-api.git
		
		AND PLEASE NOTE THAT, I've pushed the code commit by commit to my own repo https://github.com/S-Sayed/java-code-examples.git but this repo contains many projects I have done, so if you want to check the commits during the development stages, please find them here 
		https://github.com/S-Sayed/java-code-examples/commits/master/mobile-search-api
		
		- the screenshot of GIT commits history "Git Commits.JPG" is attached and it is there in the above google drive location as well
		
		- And please note that I've used the below in the implementation 
			- Java 8 features like stream, Datetime, Predicate, Lambda
			- Spring (core, boot, AOP, cache, data, test, ...)
			- Junit, Mockito
			- Design patterns
			- SOLID principles 
			
	# Running instructions
		- Please find the packaged spring boot application "mobile-search-api.jar" in the above google drive location, or you can pull the docker image "ssayed7190/sameh-public-repo:mobile-search-api" form the below docker hub link  https://hub.docker.com/r/ssayed7190/sameh-public-repo/tags 

		- To run the api
			- 1. Pre-requisites.
				- in case you will use java command, JRE should be installed 
				- in case you will use docker image, Docker should be installed 
				
			- 2. Run the application.
				- in case JAVA, please run command 
					"java -jar mobile-search-api.jar"
				
				- in case Docker, please run command 
					"docker pull ssayed7190/sameh-public-repo:mobile-search-api"
				
				- If you will checkout the code, and want to build an image, you can use the below commands 
					- to build image 
						- docker build -t ssayed7190/sameh-public-repo:mobile-search-api .
					
					- to run container 
						- docker run -it -p 8899:8899 ssayed7190/sameh-public-repo:mobile-search-api
						
				- If you will checkout the code and want to run it using maven, please run the below command
					- mvn spring-boot:run 
					
			- the spring boot will start the embedded tomcat container on port 8899
			
	# Consuming the API  
		- I have developed a HTML page + Jquery application to consume the API and display the data in table format (It is there in the above google drive location and pushed to github as well https://github.com/S-Sayed/mobile-search-api.git)  

		- To consume the api, please refer to the below sections in the "How-to-run-consume-mobile-search-api.pdf" file
			- 3. Open Mobile search Consumer Page.
			- 4. Consume the API form HTML + JQuery.
			- 5. Consume the API from the browser.
			
		- To validate the request/ response data and response header, please refer to the below sections in the "How-to-run-consume-mobile-search-api.pdf" file
			- 6. API request and response.
			
		# OpenAPI spec and Swagger UI
			- please find the "mobile-search-api-specs.yaml" file for the OpenAPI specs attached in the email and in the above google drive location and you can access the Swagger UI from this link http://localhost:8899/mobile-search-api-consumer-ui.html to consume the API
		
			- you can refer to the "How-to-run-consume-mobile-search-api.pdf" file to view the screen shots of API using swagger
			
	# Test Cases
		- To get the test cases report, please 
			- 1. checkout/ download the code from the below github repo https://github.com/S-Sayed/mobile-search-api.git, and project name is "mobile-search-api"

			- 2. make sure that maven is installed in your machine, then 
			- 3. navigate to the location of downloaded project (step #1) using cd command
			- 4. run the command "mvn surefire-report:report", then you will find the report in this location {downloadedPorjectLocation}/target/site/surefire-report.html (sample SS "Test Cases Report.JPG" is attached as well)
		
		- if you want to run the test cases, please download/ checkout the code, and run the below command 
			- mvn clean test 
			
	# Regarding high-level architecture. 
		- Please find the HLD document "Mobile-search-API-HLD.pdf" in the attached zip file/ google drive location where I described the HLD meaning and the application layers first then Sequence Diagram for the GET /mobile/search request
		
	# Points to highlight 
		- I didn't use an API gateway like ZUUL, because it is not mentioned in the task but I can use it if you want.
		
		- I didn't use service discovery like Eureka for balancing the load because the scaling is not mentioned in the task but I can use it if you want.
		
		- The following path /search?announceDate=1999&price=200 is mentioned in the task, but i think there is a typo mistake as it should be priceEur instead of price as mentioned in the first path  /search?priceEur=200. Will return 10 devices