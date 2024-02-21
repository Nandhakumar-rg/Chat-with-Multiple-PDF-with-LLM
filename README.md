Chat-with-Multiple-PDF-with-LLM

"Chat-with-Multiple-PDF-with-LLM" is a repository that likely focuses on leveraging Large Language Models (LLMs) to facilitate interactive, conversational interfaces capable of understanding and processing content from multiple PDF documents. This could involve extracting, interpreting, and responding to queries about the information contained within these PDFs, making it easier to navigate and extract insights from multiple documents simultaneously through a chat interface. This setup could be particularly useful for research, data analysis, customer support, or any scenario requiring quick access to detailed information spread across various PDF files.
#To get API KEY #Follow this link to get your own API Key and it's absolutely free. https://aistudio.google.com/app/apikey

Adding API KEY Add your API key into the .env file

Download the neccessary pacakages by running pip install -r requirements.txt

Run the app using streamlit

streamlit run app.py ##To run the pro vision model (Images).

##You can use your any favourite IDE to run this project.

Building the docker image
(Note: Run as administrator on Windows and remove "sudo" in commands)

Important - Make sure you have installed Docker on your PC:
Linux: Docker
Windows/Mac: Docker Desktop
Start Docker:
Linux (Home Directory):
sudo systemctl start docker
Windows: You can start Docker engine from Docker Desktop.
Build Docker image from the project directory:
docker build -t Image_name .
(Note: Rerun the Docker build command if you want to make any changes to the code files and redeploy.)
Running the container & removing it
witch to Home Directory:
cd ~
List the built Docker images

docker images
Start a container:
docker run -p 80:80 Image_ID
This will display the URL to access the Streamlit app (http://0.0.0.0:80). Note that this URL may not work on Windows. For Windows, go to http://localhost/.

In a different terminal window, you can check the running containers with:

docker ps
Stop the container:
Use ctrl + c or stop it from Docker Desktop.
Check all containers:
docker ps -a
Delete the container if you are not going to run this again:
docker container prune
Pushing the docker image to Docker Hub
Sign up on Docker Hub.

Create a repository on Docker Hub.

Log in to Docker Hub from the terminal. You can log in with your password or access token.

docker login
Tag your local Docker image to the Docker Hub repository:
docker tag Image_ID username/repo-name:tag
Push the local Docker image to the Docker Hub repository:
docker push username/repo-name:tag
(If you want to delete the image, you can delete the repository in Docker Hub and force delete it locally.)

Command to force delete an image (but don't do this yet):
docker rmi -f IMAGE_ID
