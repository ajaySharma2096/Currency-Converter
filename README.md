# Currency Converter - MERN Stack Application

A full stack currency converter application built with **React.js**, **Node.js**, and **MongoDB**. This application allows users to convert one currency into another using live exchange rates fetched through a backend REST API. The backend integrates with the Exchange Rates API and also stores currency data in MongoDB.

## Overview

This project is a **MERN stack currency converter** where:

- the **frontend** is built with React.js
- the **backend** is built with Node.js and Express.js
- **MongoDB** is used to store the list of currencies
- exchange rates are fetched from an external API through the backend
- the frontend communicates with the backend REST APIs to perform currency conversion

The application is designed to demonstrate full stack development concepts including API integration, REST API creation, database storage, and frontend-backend communication.

## Features

- Convert currency from one currency to another
- Fetch latest exchange rates using an external API
- React-based user interface for currency conversion
- Node.js REST API for handling conversion and currency-related operations
- Store currency list in MongoDB
- Add new currencies and persist them in the database
- Backend-controlled external API integration
- Clean separation between frontend and backend layers

## Tech Stack

### Frontend
- React.js
- JavaScript
- HTML
- CSS

### Backend
- Node.js
- Express.js

### Database
- MongoDB

### External API
- Exchange Rates API  
  `https://api.exchangeratesapi.io/latest`

## Architecture

The application follows a simple client-server architecture:

1. The user interacts with the **React frontend**
2. The frontend sends requests to the **Node.js / Express backend**
3. The backend fetches exchange rate data from the external API
4. The backend processes the conversion logic
5. MongoDB stores the currency list
6. The backend returns the response to the frontend
7. The frontend displays the converted result to the user

## Project Workflow

### Currency Conversion Flow
- User selects source currency
- User selects target currency
- User enters amount
- Frontend sends request to backend API
- Backend fetches latest exchange rates
- Backend calculates converted value
- Result is sent back to frontend
- Frontend shows converted currency amount

### Currency Management Flow
- User adds a new currency
- Frontend sends the currency data to backend
- Backend stores the currency in MongoDB
- Stored currency list can be retrieved from the database

## Folder Structure

Example project structure:

```text
currency-converter/
├── src/                 # React frontend
├── backend/                 # Node.js backend
│   ├── Route/
│   ├── Model/
│   └── DB/
│   └── index.js
├── README.md
└── package.json
```

You can update this structure section if your actual folder names are different.

## API Integration

The backend integrates with:

`https://api.exchangeratesapi.io/latest`

This external API is used to fetch current exchange rates. Instead of calling the external API directly from the frontend, the application routes requests through the backend, which helps:

- keep API handling centralized
- separate business logic from UI
- make the architecture cleaner
- improve maintainability
- make it easier to extend in the future

## Database Usage

MongoDB is used to store the list of currencies.

This allows:
- storing supported currencies
- managing custom currency entries
- persisting currency data beyond application runtime

## Installation and Setup

### Prerequisites

Make sure you have installed:
- Node.js
- npm
- MongoDB

## Clone the repository

```bash
git clone https://github.com/ajaySharma2096/Currency-Converter.git
cd Currency-Converter
```

## Install dependencies

### For backend
```bash
cd backend
npm install
```

### For frontend
```bash
npm install
```

## Environment setup

Create a `.env` file in the backend folder and add the required environment variables.

Example:

```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
```

If your project uses more variables, update this section accordingly.

## Run the application

### Start backend
```bash
cd backend
npm run watch:dev
```

### Start frontend
```bash
npm run start
```

The frontend will run on:
```text
http://localhost:3000
```

The backend will run on:
```text
http://localhost:5000
```

## Example Use Case

- Select `USD` as source currency
- Select `INR` as target currency
- Enter an amount such as `100`
- Submit the request
- The application fetches exchange rates through the backend
- The converted result is displayed on the frontend

## Possible API Endpoints

Depending on your implementation, your backend may expose endpoints like:

### Get exchange rates
```http
GET /api/rates
```

### Convert currency
```http
POST /api/convert
```

### Add new currency
```http
POST /api/currencies
```

### Get stored currencies
```http
GET /api/currencies
```

Update these endpoints to match your actual implementation.

## Key Learning Outcomes

This project demonstrates:
- full stack application development using MERN stack
- React and Node.js integration
- external API consumption
- REST API design
- MongoDB data persistence
- frontend and backend communication
- practical implementation of currency conversion logic

## Future Enhancements

Possible improvements for this project:
- add authentication and user-specific preferences
- show historical exchange rate trends
- add currency search and filtering
- improve UI/UX
- cache exchange rate data
- add validation and error handling
- write unit and integration tests
- deploy frontend and backend separately
- support favorite currencies
- add conversion history tracking

## Contributing

Contributions are welcome.

If you want to improve this project:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Commit your updates
5. Open a pull request

## License

You can add an MIT License if you want the project to be open for reuse and learning.

## Author

**Ajay Sharma**

- GitHub: https://github.com/ajaysharma3423

---

If you found this project useful, consider giving it a star.
