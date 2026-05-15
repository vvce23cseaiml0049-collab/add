https://github.com/Moulya1234/demo/tree/main


https://my.slack.com/services/new/jenkins-ci


DevOps Lab Experiment — Docker using Python
Aim---->To create a Docker image and run a Docker container using a Python application.

Requirements
Docker Desktop
VS Code
Git (optional)
STEP 1 — Create Project Folder

Create a folder named:

dockerimage

Open this folder in VS Code.

STEP 2 — Create Python File

Create a file named:

sample.py

Put this code inside:

print("Hello World")

Save the file.

STEP 3 — Create Dockerfile

Create another file named:

Dockerfile

IMPORTANT:

No extension
Not .txt

Put this code inside:

FROM python:3.10

WORKDIR /app

COPY . /app

CMD ["python", "sample.py"]

Save the file.

STEP 4 — Open Terminal

In VS Code:

Terminal → New Terminal
STEP 5 — Build Docker Image

Run:

docker build -t test1 .

Explanation:

docker build → builds Docker image
-t test1 → gives image name
. → current folder

After successful build:

Successfully tagged test1:latest
STEP 6 — Check Docker Images

Run:

docker images

Output shows:

test1
STEP 7 — Run Docker Container

Run:

docker run --name cont1 test1

Explanation:

cont1 → container name
test1 → image name

Output:

Hello World
STEP 8 — Check Containers

Run:

docker ps -a

Shows all containers.

STEP 9 — Login to Docker Hub

Run:

docker login

Enter Docker Hub:

username
password

After successful login:

Login Succeeded
STEP 10 — Tag Docker Image

Run:

docker tag test1 nairuthya/test1:latest

Explanation:

nairuthya → Docker Hub username
test1 → repository name
STEP 11 — Push Image to Docker Hub

Run:

docker push nairuthya/test1:latest

This uploads image to Docker Hub.

Output

Docker container runs successfully and displays:

Hello World
