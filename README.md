# Getting Started...

## Docker Build Instructions

Follow the instructions below to build this docker container and run the app. Please have a look at the [Docker documentation](https://docs.docker.com/) for further details.

1. Clone the repository

#### `git clone https://github.com/Abhishek-2502/Self_Checkout_AI_Shop.git`

2. Build the docker container

#### `docker build -t selfcheckout:1.0 .`

3. Run the container.
   Note: We run the container in detached mode because when the front-end starts alongiside the container. We need to execute a second command to run the backend.

#### `docker run -d --name selfcheckout -p 3000:3000 -p 5000:5000 selfcheckout:1.0`

4. Run this command to start the backend server

#### `docker exec -it selfcheckout python3 /backend_tf/app.py`

5. Open your browser and use this url

#### `http://localhost:3000`
