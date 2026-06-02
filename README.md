
# CST8919 - Lab 1: Flask App with Auth0 Integration



Setup Instructions
1. Create the Project Directory
mkdir auth0-flask-app
cd auth0-flask-app
2. Create and Activate a Virtual Environment

Windows

python -m venv venv
venv\Scripts\activate

macOS/Linux

python -m venv venv
source venv/bin/activate
3. Install Dependencies

Create a requirements.txt file:

auth0-server-python>=1.0.0b7
flask[async]>=2.0.0
python-dotenv>=1.0.0

Install the dependencies:

pip install -r requirements.txt
Configure Auth0

Sign up or log in to:

Auth0 Dashboard

Go to Applications → Applications.
Click Create Application.
Enter an application name (e.g., My Flask App) and select Regular Web Application.
In the Settings tab, configure:
Allowed Callback URLs:
http://localhost:5000/callback

Allowed Logout URLs:
http://localhost:5000

Allowed Web Origins:
http://localhost:5000
Save your changes.
Create a .env file in the project root:
AUTH0_DOMAIN=YOUR_AUTH0_DOMAIN
AUTH0_CLIENT_ID=YOUR_CLIENT_ID
AUTH0_CLIENT_SECRET=YOUR_CLIENT_SECRET
AUTH0_SECRET=YOUR_GENERATED_SECRET
AUTH0_REDIRECT_URI=http://localhost:5000/callback
Replace the placeholder values with your Auth0:
Domain
Client ID
Client Secret
Run the Application

Start the Flask application:

python app.py

Open your browser and visit:

http://localhost:5000
