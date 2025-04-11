**Documentaion**

**Output**

The output shows the results of the calculator operations in the form of JSON.

**Steps:**

Firstly, download the Git from and confirm "https://git-scm.com/" (official website).

confirm the Git by checking its version in local.

Now, pull the previous weeks code from the repository "https://github.com/vivekolladapu/sit737-2025-prac5p.git" to local.

Make sure that the project structure should be as below,

sit737-2025-prac5d |--node_modules |--logs | |--(combined.log) | |--(error.log) |--server.js |-Dockerfile |--docker-compose.yml |--package.json |--package-lock.json |--README.md

Now, build and run with Docker Compose by using "docker-compose up --build".

Check the application at "http://localhost:3020/add?num1=5&num2=10".

Now, stop the docker by using "docker-compose down".

Now, download the google cloud CLI, and confirm the download by checking it version.

Then, initialize it by using "gcloud init".

After this, authenticate with google cloud by using "gcloud auth login".

Now, setup the config to project by using "gcloud config set <Project_ID>".

create the artifact registry by using "gcloud artifacts repositories create prac5d-repo \
  --repository-format=docker \
  --location=australia-southeast1 \
  --description="Docker repo for SIT737 prac5d"".

Then, authenticate the docker with artifact registry by using "gcloud auth configure-docker australia-southeast1-docker.pkg.dev".

Now, tag the image by using "docker tag <Image_ID> australia-southeast1-docker.pkg.dev/<Project_ID>/prac5d-repo/prac5d-calculator:latest".

Then push the image to the artifact registry by using "docker push australia-southeast1-docker.pkg.dev/<Project_ID>/prac5d-repo/prac5d-calculator:latest".

Now, run the image from the artifact registry by using "docker run -p 3020:3020 australia-southeast1-docker.pkg.dev/<Project_ID>/prac5d-repo/prac5d-calculator:latest".

Push the code to the git by creating a new repository with "sit737-2025-prac5d".

Add all the files by using "git add .".

Commit the changes by using "git commit -m"initial commit"".

Push it to the Git by using "Git push".
