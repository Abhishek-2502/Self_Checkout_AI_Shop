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




# Self Checkout AI Shop

Welcome to the Self Checkout AI Shop! This project is an AI-powered self-checkout system that lets users take a photo of themselves with a product. The AI model identifies the product and adds it to the cart with the price and quantity. The application is built with Flask (backend), React (frontend), and is containerized with Docker.

## Features

- **AI Product Identification**: Identifies products from images taken by users.
- **Cart Management**: Adds identified products to the user's cart with price and quantity.
- **Dockerized**: Deploys easily using Docker.
- **Cross-Platform**: Access the application through a web browser on any platform.

## Getting Started

Follow these steps to build and run the application using Docker:

1. **Clone the Repository**: Clone the repository to your local machine.
    ```bash
    git clone https://github.com/Abhishek-2502/Self_Checkout_AI_Shop.git
    cd Self_Checkout_AI_Shop
    ```

2. **Build the Docker Container**: Run this command to build the Docker container.
    ```bash
    docker build -t selfcheckout:1.0 .
    ```

3. **Run the Docker Container**: Run the Docker container in detached mode and map the necessary ports.
    ```bash
    docker run -d --name selfcheckout -p 3000:3000 -p 5000:5000 selfcheckout:1.0
    ```

4. **Start the Backend Server**: Execute the backend server inside the running container.
    ```bash
    docker exec -it selfcheckout python3 /backend_tf/app.py
    ```

5. **Access the Application**: Open your web browser and go to [http://localhost:3000](http://localhost:3000).

## How to Use

1. **Camera Access**: Allow camera access when prompted.
2. **Capture Image**: Capture an image of yourself with the product.
3. **Product Identification**: The AI model identifies the product in the image.
4. **Add to Cart**: The identified product is added to your cart with price and quantity.
5. **Checkout**: Follow the checkout process on the UI to complete your purchase.

## Contributing

Contributions, bug reports, and feature requests are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Special thanks to all open-source contributors.
- Thanks to the creators and maintainers of the technologies used in this project.
