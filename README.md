# Email API

This is a simple email-sending API built with Node.js and Express, designed to handle contact form submissions from a portfolio website. It uses **Nodemailer** for sending emails and **CORS** to allow requests from a different domain.

## Features

- Send emails using a contact form

- Validation of inputs to ensure all fields are filled

- Protected against spamming via rate-limiting

- Deployed on Heroku

## Installation

1\. Clone the repository:

```bash
    git clone https://github.com/your-username/email-api.git
```

2\. Navigate to the project directory:

```bash
    cd email-api
```

3\. Install dependencies:

```bash
    npm install
```

4\. Create a `.env` file and configure your environment variables:

```bash
    EMAIL_USER=your-email@gmail.com
    EMAIL_PASS=your-email-password
    EMAIL_SERVICE=gmail
```

## Usage

To start the server locally:

```bash
npm start
```


The API will be running on `http://localhost:5000`.

### API Endpoint

#### Send Email

-   **URL:** `/api/send-email`

-   **Method:** `POST`

-   **Content-Type:** `application/json`

-   **Request Body:**

```json
{
  "name": "John Doe",
  "email": "johndoe@example.com",
  "message": "Hello, I am interested in your work."
}
```


### Response:

-   **Success (200):**

```json
{
  "message": "Email sent successfully!"
}
```


-   **Error (400 or 500):**

```json
{
  "message": "Failed to send email."
}
```

----------

## Deployment

This project is ready to be deployed on Heroku. Make sure to configure your environment variables in the Heroku dashboard.

### To deploy:

1\.  Login to Heroku:

```bash
    heroku login
```

2\.  Push the repository to Heroku:

```bash
    git push heroku main
```

------------

## Dependencies

-   [Express](https://expressjs.com/)

-   Nodemailer

-   [dotenv](https://github.com/motdotla/dotenv)

-   [CORS](https://github.com/expressjs/cors)

-   [Joi](https://joi.dev/)

-   [Morgan](https://github.com/expressjs/morgan)

-------

License

This project is licensed under the MIT License.
