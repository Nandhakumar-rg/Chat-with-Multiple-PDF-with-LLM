# Chat-with-Multiple-PDF-with-LLM
Chat-with-Multiple-PDF-with-LLM" is a repository that likely focuses on leveraging Large Language Models (LLMs) to facilitate interactive, conversational interfaces capable of understanding and processing content from multiple PDF documents. This could involve extracting, interpreting, and responding to queries about the information contained within these PDFs, making it easier to navigate and extract insights from multiple documents simultaneously through a chat interface. This setup could be particularly useful for research, data analysis, customer support, or any scenario requiring quick access to detailed information spread across various PDF files. 

#To get API KEY
#Follow this link to get your own API Key and it's absolutely free.
https://aistudio.google.com/app/apikey

Adding API KEY
Add your API key into the .env file

1. Download the neccessary pacakages by running
pip install -r requirements.txt

2. Run the app using streamlit

streamlit run Gemini_Pro_Vision.py  ##To run the pro vision model (Images).

streamlit run app.py  ##To run the model.

### Building the docker image

(Note: Run as administrator on Windows and remove "sudo" in commands)

3. Important - Make sure you have installed Docker on your PC:
- Linux: Docker
- Windows/Mac: Docker Desktop

4. Start Docker:
- Linux (Home Directory):
  ```
  sudo systemctl start docker
  ```
- Windows: You can start Docker engine from Docker Desktop.

5. Build Docker image from the project directory:

```commandline
docker build -t Image_name .
```

### (Note: Rerun the Docker build command if you want to make any changes to the code files and redeploy.)

### Running the container & removing it

6. witch to Home Directory:

```
cd ~
```
List the built Docker images
```
docker images
```

7. Start a container:
```commandline
docker run -p 80:80 Image_ID
```

8. This will display the URL to access the Streamlit app (http://0.0.0.0:80). Note that this URL may not work on Windows. For Windows, go to http://localhost/.

9. In a different terminal window, you can check the running containers with:
```
docker ps
```

10. Stop the container:
 - Use `ctrl + c` or stop it from Docker Desktop.

11. Check all containers:
 ```
docker ps -a
 ```

12. Delete the container if you are not going to run this again:
 ```
 docker container prune
 ```

### Pushing the docker image to Docker Hub

13. Sign up on Docker Hub.

14. Create a repository on Docker Hub.

15. Log in to Docker Hub from the terminal. You can log in with your password or access token.
```
docker login
```

17. Tag your local Docker image to the Docker Hub repository:
 ```
docker tag Image_ID username/repo-name:tag
 ```

17. Push the local Docker image to the Docker Hub repository:
 ```
 docker push username/repo-name:tag
 ```

(If you want to delete the image, you can delete the repository in Docker Hub and force delete it locally.)

18. Command to force delete an image (but don't do this yet):
 ```
docker rmi -f IMAGE_ID
 ```
