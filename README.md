# Airalo API Automation

## Overview
This project contains automated tests for the Airalo API using Postman. The tests validate various API endpoints, including authentication, order creation, and eSIM retrieval. The goal is to ensure the API behaves as expected and to catch any issues early.

## Prerequisites

### Software Requirements
- [Postman](https://www.postman.com/downloads/) (latest version)
- [Node.js] (https://nodejs.org/) (if using Newman for command-line execution)

### Environment Setup
1. Install Postman:
   - Download and install Postman from the official website.

2. Install Newman (Optional):
   - If you plan to run tests via the command line, install Newman globally:
     npm install -g newman

## Configuration
### Environment Variables
Ensure you have set up the following environment variables in Postman: 
- **`baseURL`**: Base URL for the API (e.g., `https://sandbox-partners-api.airalo.com `). 
- **`clientID`**: Your client ID for OAuth2 authentication.
- **`clientSecret`**: Your client secret for OAuth2 authentication.
- **`maxQuantity`**: The maximum supported quantity of items in the order.
- **`exceedingMaxQuantity`**: The quantity more than the supported quantity of items in the order.
- **`simPackageID`**: The package ID associated with the order.
- **`packageType`**: type of package (e.g., `sim `).


## Test Cases
### Test Case Summary
For a detailed list of test cases, including descriptions, priorities, and steps, refer to the [Test Cases CSV Sheet](API_TestCases.csv). 


### Key Test Cases 

Here are some key test cases to give an overview: -

- **Authentication Test:**
- **Description:** Verify that the OAuth2 token can be successfully retrieved.
 - **Expected Result:** Status `200 OK` with a valid access token.

- **Order Creation Test:** 
- **Description:** Verify the creation of an order for the eSIM package. 
- **Expected Result:** Status `200 OK` for a successful order creation. 

- **eSIM Retrieval Test:**
 - **Description:** Ensure that the list of eSIMs can be retrieved correctly.
 - **Expected Result:** Status `200 OK` with the correct list of eSIMs.

## Getting Started

### Importing the Collection
1. Open Postman.
2. Go to the "Collections" tab on the left sidebar.
3. Click on "Import" and upload the ` AiraloAPIsValidation.postman_collection.json `  file.

### Running Tests in Postman
1. Select the ` AiraloAPIsValidation ` collection from the Collections tab.
2. Click on the **“Runner” ** button located in the Postman footer, at the bottom of the interface.
3. Configure the Collection Runner:
   - **Data File:** Optionally, upload a data file if your collection uses data-driven tests.
   - **Iterations:** Set the number of iterations if running tests multiple times.
   - **Delay:** Add a delay between requests if needed.
4. Click **“Run”** to execute the tests.

### Running Tests with Newman (Optional)
To run the tests via the command line:
newman run AiraloAPIsValidation.postman_collection.json

### Documentation

- [API Documentation](API_Automation_Documentation.docx)