# California house pricing

# House Price Prediction in California

![end-to-end-ml-project drawio](https://github.com/satishkolli1992/californiahousepricing/assets/40614187/defba9a5-4606-4d14-8c38-9a37a75772f3)

This project implements an end-to-end machine learning solution for predicting house prices in California. It consists of the following key components:

## Linear Regression Model: 
In the first step, a Linear Regression machine learning model is developed using Python. The model is trained on a dataset containing various features of houses, such as location, number of bedrooms, square footage, and more. The trained model is saved as a pickle file for later use.

## Web Application:
A web application is created using the Flask framework. This application allows users to input information about a house and receive a predicted price based on the trained Linear Regression model. The web interface is intuitive and user-friendly, making it easy for anyone to get house price predictions.

## Dockerization:
The entire web application is containerized using Docker. This means that you can package the application and its dependencies into a Docker image, ensuring consistent and reliable deployment across different environments.

## Deployment on Heroku:
The Dockerized web application is deployed on the Heroku platform. Heroku provides a convenient and scalable platform for hosting web applications, making it accessible to users on the internet.

How to Use
To use this project, follow these steps:

## Setup
To set up this project locally, follow these steps:

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/satishkolli1992/californiahousepricing.git
   ```

2. Create a virtual environment (recommended) and install the dependencies:

   ```bash
   cd californiahousepricing
   python -m venv venv
   source venv/bin/activate  # On Windows, use: venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. Run the Flask application locally:

   ```bash
   python app/app.py
   ```

   You can access the web application by opening a browser and navigating to http://localhost:5000.



## Linear Regression Model
The Linear Regression model was developed using the Jupyter notebook `californiahousepricing
/Linear regression - ML Implementation - California Housing.ipynb.ipynb`. The trained model is saved as `californiahousepricing/regmodel.pkl`. This model is used for making house price predictions in the web application.

## Web Application
The web application is built using the Flask framework and allows users to input various features of a house and get a predicted price. The main files for the web application are located in the `app/` directory. The application include a HTML templates (`home.html`) and Python code in `app.py`.

## Dockerization
To run the application in a Docker container, use the provided `Dockerfile`. You can build the Docker image and run the container locally using Docker Desktop or a similar tool.

```bash
docker build -t californiahousepricing .
docker run -p 5000:5000 californiahousepricing
```

## Deployment on Heroku
The web application is deployed on Heroku as a Docker container. To deploy your own version of this application on Heroku, follow these general steps:

1. Create a Heroku account and install the Heroku CLI if you haven't already.

2. Log in to Heroku using the CLI:

   ```bash
   heroku login
   ```

3. Navigate to the project directory and create a Heroku app:

   ```bash
   heroku create your-app-name
   ```

4. Push the Docker container to Heroku:

   ```bash
   heroku container:push web -a your-app-name
   ```

5. Release the container:

   ```bash
   heroku container:release web -a your-app-name
   ```

6. Open your Heroku app in the browser:

   ```bash
   heroku open -a your-app-name
   ```

Now, your California House Price Prediction web application is live on Heroku!

Feel free to customize and improve this project as needed. Happy coding!
