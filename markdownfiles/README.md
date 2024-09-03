### TASK1:
- Created Dockerfile which helps in building the image required for the Application
- Built the docker file using the below command
        
        docker build -t sample-api .
        
- Pushed the docker image to docker hub using below commands:
        
        docker tag sample-api srivyshnavi01/sample-api:latest
        
        docker push srivyshnavi01/sample-api:latest
### Task2:

- Created Github Workflow and ran the unit tests and build the image using the
Dockerfile that I have created and published the image to the GitHub container
registry (ghcr.io) for both linux/amd64 and 
linux/arm64 architectures.

- To download the docker image from the github repository use the below command:

        docker pull ghcr.io/srivyshnavi01/sample-api:latest

- To run the docker image in local, user need to use the below command.

            docker run -d -p 3000:3000 ghcr.io/srivyshnavi01/sample-api:latest

- Instruction on how to trigger and run the Github workflow.:

        1. User need to navigate to the Actions Tab of their GitHub repository.
        2. Select the Workflow we want to check.
        3. Ensure the latest run shows all jobs completed successfully. we should see green checkmarks indicating success.
        4. According to the workflow that we have configured, build will get triggered for each and every chnage we push to github.

                 My workflow link : https://github.com/srivyshnavi01/sample-api/actions
  
       
        5.Manually Triggering the Workflow:

          - Go to the Actions tab of our repository.
          - Select the workflow we want to run.
          - Click on the “Run workflow” button.

- Added the images of the successful run of the builds.

