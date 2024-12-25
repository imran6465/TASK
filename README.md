# TASK

# Twitter Trending Topics Scraper

This project fetches the top 5 trending topics from Twitter and saves the data to a MongoDB database. It also uses ProxyMesh to ensure that each new request is sent from a different IP address.

## Setup Instructions

### Prerequisites
Make sure you have the following installed:
- Node.js (v14 or higher)
- MongoDB (local or remote instance)

### Installation Steps

1. **Clone the repository:**

```bash
git clone https://github.com/your-repository/twitter-trending-scraper.git
cd twitter-trending-scraper
```

2. **Install dependencies:**

```bash
npm install
```

3. **Setup environment variables:**

Create a `.env` file in the root directory of the project and add your Twitter login credentials:

```env
TWITTER_USERNAME
TWITTER_EMAIL_OR_PHONE
TWITTER_PASSWORD=
PROXYMESH_USERNAME
PROXYMESH_PASSWORD
PROXYMESH_ENDPOINT
```

4. **Run the server:**

```bash
node server.js
```

The server will start on `http://localhost:3000`.

### Routes

- **GET `/`**: Renders the `index.ejs` page.
- **POST `/run-script`**: Triggers the script to fetch trending topics and save them to MongoDB. Returns the trending topics, IP address used, and the MongoDB record.

### MongoDB 

#for local mongodb database setup
- create a directory for storing data
- install mongodb
- edit environmental variables and add to the system path 
- run this command
```bash
mongod --dbpath <path_to_your_directory>
```

### Notes

- The project uses the `dotenv` package to load sensitive credentials from a `.env` file.
- The ProxyMesh credentials are set to route each request through a different IP address.


