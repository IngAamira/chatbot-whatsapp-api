# MedPet

MedPet is an online pet store chatbot service that integrates with WhatsApp to provide users with assistance, appointment scheduling, and other functionalities. It also integrates with Google Sheets for storing appointment data and OpenAI for answering user queries.

## Table of Contents

1. [Introduction](#medpet)
2. [Features](#features)
3. [Project Structure](#project-structure)
4. [Prerequisites](#prerequisites)
5. [Installation](#installation)
6. [Configuration Environment Variables](#configuration-environment-variables)
7. [Usage](#usage)
   - [Development Mode](#development-mode)
   - [Production Mode](#production-mode)
8. [API Endpoints](#api-endpoints)
   - [Webhook](#webhook)
9. [Dependencies](#dependencies)
10. [License](#license)
11. [Author](#author)

## Features

- **WhatsApp Integration**: Communicate with users via WhatsApp using interactive buttons, media messages, and location sharing.
- **Appointment Scheduling**: Users can schedule appointments for their pets, and the data is stored in Google Sheets.
- **AI Assistance**: Provides answers to user queries using OpenAI's GPT-4 model.
- **Google Sheets Integration**: Stores appointment data in a Google Sheet for easy access and management.

## Project Structure

## Prerequisites

- Node.js (v16 or higher)
- npm
- A WhatsApp Business API account
- Google Cloud credentials for accessing Google Sheets
- OpenAI API key

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/medpet.git
   cd medpet
   npm install
    ```

## Configuration Environment Variables
1. Configure environment variables: Create a .env file in the src/config directory and add the following:
```js
BASE_URL=https://graph.facebook.com
API_VERSION=v16.0
BUSINESS_PHONE=your_business_phone_id
API_TOKEN=your_whatsapp_api_token
WEBHOOK_VERIFY_TOKEN=your_webhook_verify_token
OPENAI_API_KEY=your_openai_api_key
Add your Google Cloud credentials: Replace the content of src/credentials/credentials.json with your Google Cloud service account credentials.
```
2. Add your Google Cloud credentials: Replace the content of `src/credentials/credentials.json` with your Google Cloud service account credentials.

## Usage
### Development Mode
Start the application in development mode with nodemon:
   ```bash
   npm run dev
   ```

### Production Mode
Start the application in production mode:
   ```bash
   npm start
   ```

## API Endpoints

### Webhook
* POST /webhook: Handles incoming messages from WhatsApp.
* GET /webhook: Verifies the webhook with the provided token.

### Dependencies
* express: Web framework for handling HTTP requests.
* axios: For making HTTP requests to external APIs.
* dotenv: For managing environment variables.
* googleapis: For interacting with Google Sheets.
* openai: For AI-powered responses.
* nodemon (dev dependency): For automatic server restarts during development.

## License
This project is licensed under the ISC License.

## Author
Developed by [IngAamira](https://ingaamira.github.io/)