ReqRes API Testing Project
This repository contains a professional API testing framework for the ReqRes API. The project leverages Postman for designing and executing test cases, Newman for automated test execution, Jenkins for CI/CD pipeline integration, and HTML Report for generating comprehensive test result reports.

Project Overview
ReqRes provides a free API for testing and prototyping. This project automates testing for various endpoints and scenarios using best practices in API testing, including parameterized test cases and environment-based configurations.

Features
Environment Files: Utilizes Postman environment files to manage base URLs and variables dynamically.
Automated Testing: Runs tests via Newman for seamless automation and integration into pipelines.
Jenkins Integration: Automates test execution using Jenkins, allowing continuous integration and delivery.
HTML Reports: Generates visually rich reports with detailed insights into test results.
Endpoints Covered
User Management

GET /api/users?page=2 - Fetches paginated user data.
POST /api/users - Creates a new user.
PUT /api/users/{id} - Updates user data.
DELETE /api/users/{id} - Deletes a user.
Authentication

POST /api/login - Validates login with valid credentials.
POST /api/register - Registers a new user.
Error Scenarios

POST /api/login - Tests invalid login credentials.
POST /api/register - Tests missing fields for registration.
Setup Instructions
Pre-requisites
Install Node.js and npm.
Install Newman:
bash
Copy code
npm install -g newman
Install HTML Reporter for Newman:
bash
Copy code
npm install -g newman-reporter-html
Clone the Repository
bash
Copy code
git clone <repository-url>
cd <repository-folder>
Environment Setup
Configure the Postman environment file with the following:
Base URL: https://reqres.in
Any other necessary variables (e.g., userId, token).
Run Tests Locally
Using Newman
Execute the following command to run tests and generate an HTML report:

bash
Copy code
newman run Postman_Collection.json -e Postman_Environment.json -r html --reporter-html-export ./reports/TestReport.html
Integrating with Jenkins
Create a New Jenkins Job:

Type: Freestyle Project or Pipeline.
Add steps to pull this repository and execute Newman.
Shell Command for Jenkins:

bash
Copy code
newman run Postman_Collection.json -e Postman_Environment.json -r html --reporter-html-export ./reports/TestReport.html
Archive HTML Report:

Use the "Post-build Actions" in Jenkins to archive the generated HTML report.
Test Reporting
HTML reports are automatically generated and stored in the ./reports folder.
Reports include:
Passed and failed test cases.
Response times and status codes.
Comprehensive error details for debugging.
Contributing
Feel free to fork this repository, make your contributions, and create a pull request. For major changes, open an issue to discuss your proposal.

License
This project is licensed under the MIT License.

Contact
For any queries or suggestions, please contact the project maintainer paula.farid9@gmail.com






