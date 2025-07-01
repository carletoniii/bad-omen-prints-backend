Bad Omen Prints – Backend
This is the backend for Bad Omen Prints, a custom film photography storefront built with Shopify Hydrogen. This Express.js server handles email subscriber submissions and writes them to a PostgreSQL database hosted on Railway.

Tech Stack
Node.js

Express.js

PostgreSQL (Railway)

pg (Node PostgreSQL client)

dotenv

CORS

Deployed on Railway

Features
POST /api/subscribe: Accepts a JSON payload with an email address and stores it in the email_subscribers table

Handles duplicate email entries with a clean 409 response

Automatically ignores invalid or missing data

Local Development
Clone the repo

git clone https://github.com/carletoniii/bad-omen-prints-backend.git
cd bad-omen-prints-backend

Install dependencies

npm install

Add a .env file to the root directory with the following values:

PORT=3001
DATABASE_URL=postgresql://username:password@host:port/dbname

(Never commit this file — it should be excluded by .gitignore)

Run the server

npm start

Your backend will be running at http://localhost:3001

Deployment (Railway)
Link your GitHub repo to a new project in Railway

Set your environment variables (PORT, DATABASE_URL) under the Variables tab

Railway will automatically deploy on each push to main

License
MIT — feel free to fork and use responsibly.