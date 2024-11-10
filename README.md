# 🌱 Plantsy App

Welcome to **Plantsy**! This is a plant store app that allows users to view, add, search, update, and delete plants from an inventory. This project was built for the admin side of a plant store to manage the plant catalog.

## Table of Contents

- [Project Overview](#project-overview)
- [Setup Instructions](#setup-instructions)
- [Features](#features)
  - [Core Features](#core-features)
  - [Advanced Features](#advanced-features)
- [Usage](#usage)
- [Endpoints](#endpoints)
- [Technologies Used](#technologies-used)
- [Deployment](#deployment)

## Project Overview

Plantsy is a React-based web application that interacts with a backend API to manage plant data. The app allows users to:

- View all plants.
- Add new plants.
- Mark plants as sold out.
- Search for plants by name.
- Update the price of plants.
- Delete plants.

The application is built using **React** for the frontend and a JSON server to handle backend data.

## Setup Instructions

### 1. Clone the repository

```bash
git clone <https://github.com/Njijinoela/react-hooks-cc-plantshop.git>
cd react-hooks-cc-plantshop
```

### 2. Install dependencies

Run the following command to install all the necessary dependencies:

```bash
npm install
```

### 3. Start the JSON Server

Start the JSON server to handle backend API requests. The server will run on `http://localhost:6001`.

```bash
npm run server
```

This will run the backend server on port `6001`. You can visit `http://localhost:6001/plants` to verify the backend is working.

### 4. Start the React App

In a new terminal window, run:

```bash
npm start
```

This will run the app on `http://localhost:3000`.

### 5. Open the App

Visit `http://localhost:3000` in your browser to view the app.

## Features

### Core Features

1. **View All Plants**: When the app starts, all plants are loaded from the backend and displayed.
2. **Add a New Plant**: Users can add new plants to the inventory using the provided form. The plant will be immediately added to the list and saved to the backend.
3. **Mark as Sold Out**: Users can toggle the availability of each plant. If a plant is in stock, it will be marked "In Stock", otherwise, "Out of Stock."
4. **Search for Plants**: Users can search for plants by name using the search bar, which filters the displayed list of plants.

### Advanced Features

1. **Update Plant Price**: Users can update the price of any plant directly from the plant card. The updated price is persisted to the backend.
2. **Delete a Plant**: Users can delete a plant from the inventory, and it will be removed from the list and the backend.

## Usage

### Add a Plant

To add a plant, fill in the "Plant Name", "Image URL", and "Price" in the form at the top of the page, then click **Add Plant**. The new plant will be added to the list.

### Search for Plants

Use the search bar to filter plants by typing part of their name. The plant list updates dynamically as you type.

### Update Plant Price

In the plant card, type a new price into the price input field, then click **Update Price** to save the updated price. This change will persist in the backend.

### Mark a Plant as Sold Out

Each plant card has an **In Stock** button. Clicking it toggles the plant between "In Stock" and "Out of Stock".

### Delete a Plant

Click the **Delete** button in the plant card to remove a plant from the inventory.

## Endpoints

The app interacts with a local JSON server at `http://localhost:6001`. Below are the key API endpoints used in the app:

### GET `/plants`

Retrieves the list of all plants.

#### Example Response:

```json
[
  {
    "id": 1,
    "name": "Aloe",
    "image": "./images/aloe.jpg",
    "price": 15.99
  },
  {
    "id": 2,
    "name": "ZZ Plant",
    "image": "./images/zz-plant.jpg",
    "price": 25.98
  }
]
```

### POST `/plants`

Adds a new plant to the list.

#### Request Headers:

```json
{
  "Content-Type": "application/json"
}
```

#### Request Body Example:

```json
{
  "name": "Snake Plant",
  "image": "./images/snake-plant.jpg",
  "price": 30.0
}
```

#### Example Response:

```json
{
  "id": 3,
  "name": "Snake Plant",
  "image": "./images/snake-plant.jpg",
  "price": 30.0
}
```

### PATCH `/plants/:id`

Updates the price of a plant.

#### Request Body Example:

```json
{
  "price": 35.0
}
```

### DELETE `/plants/:id`

Deletes a plant from the list.

#### Example Response:

```json
{}
```

## Technologies Used

- **Frontend**: React, HTML, CSS, JavaScript.
- **Backend**: JSON Server for simulating a REST API.
- **Tools**: npm, Fetch API.

## Deployment

The app is deployed and accessible via this live link:  
[Plantsy Live](https://spontaneous-sunshine-b01107.netlify.app/)

## License

This project is licensed under the MIT License.
