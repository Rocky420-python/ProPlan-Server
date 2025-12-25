ProPlan-Server
ProPlan-Server is a RESTful API backend built with Flask to manage user authentication and other related functionalities. It handles user login, registration, and data management for the ProPlan application.

Table of Contents
Features
Prerequisites
Installation
Usage
API Endpoints
File Structure
Contributing
License
Features
User Login authentication
JSON data storage for users
Basic validation for user inputs
Error handling
Prerequisites
Python 3.8+
Flask
json module (comes with Python)
Optional: virtual environment for isolated setup
Installation
Clone the repository:
CopyRun
git clone https://github.com/yourusername/ProPlan-Server.git
cd ProPlan-Server
Create and activate a virtual environment (optional but recommended):
CopyRun
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install the required dependencies:
CopyRun
pip install Flask
Usage
Ensure your User.json file exists in the root directory with the appropriate user data structure:
CopyRun
[
  {
    "username": "user123",
    "password": "pass123"
  }
]
Run the Flask app:
CopyRun
python app.py
Access the API endpoint:
CopyRun
GET http://localhost:5000/login?username=yourusername&password=yourpassword
API Endpoints
GET /login
Authenticate a user based on username and password.

Query Parameters:

username (string): The username of the user (6-8 characters).
password (string): The password of the user (6-8 characters).
Response:

Success or error message in JSON format.
File Structure
CopyRun
ProPlan-Server/
│
├── app.py                # Main application file
├── User.json             # User data storage
├── README.md             # This file
└── requirements.txt      # Dependencies (optional)
Contributing
Contributions are welcome! Please fork the repository and create a pull request with your improvements.

License
This project is licensed under the MIT License. See the LICENSE file for details.

