# URL Shortener API

This is an URL shortener service . Only the backend part is covered here. 
The API service can take a long URL and convert it to a shorter URL.The long URL, short URL, and other details are stored in the database. When a long URL that is already stored in the database is passed again, it returns the older shortened URL.

## Run Locally

Clone the project

```bash
  git clone https://github.com/Aniketsinghcoder/URL-Shortener.git
```

Go to the project directory

```bash
  cd URL-Shortener
```

Install dependencies

```bash
  npm install
```

Start the server

```bash
  node app.js
```

## API Reference

### Shorten URL

```http
  POST /api/short
```

| Field | Type   | Description  |
| :---- | :----- | :----------- |
| Body  | `json` | Original Url |

**Example:**

```http
POST http://localhost:3333/api/short
Content-Type: application/json

{
    "origUrl": "https://www.google.com/"
}

```


## Environment Variables

Because we have used MongoDB, we’ll need a MongoDB SRV URI. You can create a database from this [link](https://www.mongodb.com/cloud/atlas). 

Now, create a `.env` file  to store the MongoDB SRV URI and the base URL, to run this project. The base URL will be your local host server location for now. Here’s my .env file code:

```
MONGO_URI=mongodb+srv://username:password@cluster0.mkws3.mongodb.net/DB_NAME?retryWrites=true&w=majority
BASE=http://localhost:3333
```

Remember to change the ```<username> , <password> & <DB_NAME>``` field in the MongoDB URI with your database username , password & database name.

## Working of REST API 

![WORKING_GIF](working_image.gif)

## Tech Stack

![NodeJS](https://img.icons8.com/color/65/nodejs.png) **NodeJS** | ![ExpressJS](https://www.vectorlogo.zone/logos/expressjs/expressjs-icon.svg) **ExpressJS** | ![MongoDB](https://img.icons8.com/color/65/000000/mongodb.png)**MongoDB**
|:---:|:---:|:---:|
