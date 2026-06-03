
# CST8919 - Lab 1: Flask App with Auth0 Integration

**Student Name**: Naveed Hossain
**Student ID**: 0410818822 
**Course**: CST8919 DevOps - Security and Compliance
**Semester**: Spring/Summer 2026

---

## Demo Video

https://www.youtube.com/watch?v=Mco-l7PuNp0

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

### 2. Create a Virtual Environment

**Windows**

```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Install Dependencies

Create a `requirements.txt` file with the following dependencies:

```txt
auth0-server-python>=1.0.0b7
flask[async]>=2.0.0
python-dotenv>=1.0.0
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

---

## Auth0 Configuration

### Create an Auth0 Application

1. Log in to the Auth0 Dashboard.
2. Navigate to **Applications → Applications**.
3. Click **Create Application**.
4. Enter a name for your application.
5. Select **Regular Web Application**.
6. Click **Create**.

### Configure Application Settings

In the **Settings** tab, configure the following URLs:

```text
Allowed Callback URLs:
http://localhost:5000/callback

Allowed Logout URLs:
http://localhost:5000

Allowed Web Origins:
http://localhost:5000
```

Click **Save Changes**.

---

## Environment Variables

Create a `.env` file in the project root directory:

```env
AUTH0_DOMAIN=YOUR_AUTH0_DOMAIN
AUTH0_CLIENT_ID=YOUR_CLIENT_ID
AUTH0_CLIENT_SECRET=YOUR_CLIENT_SECRET
AUTH0_SECRET=YOUR_GENERATED_SECRET
AUTH0_REDIRECT_URI=http://localhost:5000/callback
```

Replace the placeholder values with the credentials from your Auth0 application settings.

---

## Running the Application

Start the Flask application:

```bash
python app.py
```

Open your browser and navigate to:

```text
http://localhost:5000
```

