# 🔎 Price Scout

**Price Scout** is a full-stack web-based product price comparison platform that helps users search and compare products across **Amazon and Flipkart**.

The application provides product information such as price, MRP, discount, ratings, reviews, product images, and shopping links, allowing users to make informed purchasing decisions.

---

## 🚀 Features

* 🔍 Product search
* 🏷️ Category-based product filtering
* 🔤 Keyword and synonym-based search
* 🛒 Amazon and Flipkart shopping links
* 💰 Product price and MRP comparison
* 📉 Discount percentage calculation
* ⭐ Product ratings and review counts
* 🖼️ Product images
* 👤 User registration and login
* 📦 Order placement and order history
* 🌐 RESTful API architecture
* 🔄 CORS-enabled frontend-backend communication
* ⚡ Nodemon for development

---

## 📂 Product Categories

Price Scout currently supports:

* 💻 Laptops
* 📱 Smartphones
* 🎧 Headphones
* 📺 Televisions
* ❄️ Refrigerators

Each category contains multiple products with comparison information.

---

## 🛠️ Technologies Used

### Frontend

* HTML5
* CSS3
* JavaScript

### Backend

* Node.js
* Express.js

### APIs & Data

* REST APIs
* JSON
* CORS

### Development Tool

* Nodemon

---

## 🏗️ Project Architecture

```text
                    Price Scout
                        │
              ┌─────────┴─────────┐
              │                   │
          Frontend              Backend
        HTML/CSS/JS          Node.js + Express
              │                   │
              └──── REST API ─────┘
                        │
                Product Catalogue
                        │
              ┌─────────┴─────────┐
              │                   │
           Search             Categories
              │                   │
              └─────────┬─────────┘
                        │
                 Product Results
                        │
                Amazon / Flipkart
                    Shopping Links
```

---

## 🔍 How Product Search Works

When a user searches for a product, the frontend sends a request to the backend:

```text
GET /api/search?q=laptop
```

The backend processes the search query and identifies the appropriate product category.

The application also supports synonyms. For example:

```text
phone     → smartphone
mobile    → smartphone
iphone    → smartphone
fridge    → refrigerator
tv        → television
earphone  → headphones
earbud    → headphones
headset   → headphones
```

The backend then returns the matching products as JSON.

---

## 📡 API Endpoints

### Search Products

```http
GET /api/search?q=laptop
```

Returns products matching the search query.

### Get Categories

```http
GET /api/categories
```

Returns the available product categories.

### Register User

```http
POST /api/register
```

Creates a new user account.

Example request:

```json
{
  "name": "John",
  "email": "john@example.com",
  "password": "password123"
}
```

### Login

```http
POST /api/login
```

Authenticates a registered user.

### Place Order

```http
POST /api/order
```

Creates a new order.

### Get User Orders

```http
GET /api/orders/:email
```

Returns the order history of a user.

---

## 📊 Product Information

Each product contains information such as:

```text
Product ID
Product Name
Product Image
Price
MRP
Rating
Number of Reviews
Amazon Link
Flipkart Link
Discount Percentage
```

The discount percentage is calculated by the backend using:

```text
Discount % = ((MRP - Price) / MRP) × 100
```

---

## 🔐 User Authentication

Price Scout provides basic user registration and login functionality.

### Registration

```text
User
 ↓
Registration Form
 ↓
POST /api/register
 ↓
Express Backend
 ↓
User Created
```

### Login

```text
User
 ↓
Login Form
 ↓
POST /api/login
 ↓
Backend Validation
 ↓
Login Successful
```

---

## 📦 Order Management

Users can place orders through the application.

The order system stores information such as:

* Order ID
* Product ID
* Product name
* Store
* Price
* Payment method
* Order status
* Order date
* Expected delivery date

The backend generates a unique order ID for each order.

Example:

```text
PS1001
PS1002
PS1003
```

---

## 🌐 Amazon & Flipkart Integration

Price Scout provides direct shopping/search links for products on Amazon and Flipkart.

The application does **not act as a replacement for these shopping platforms**. Instead, it provides comparison information and allows users to continue their shopping through the available links.

---

## 📁 Project Structure

```text
PriceScout/
│
├── public/
│   ├── index.html
│   ├── css/
│   ├── js/
│   └── assets/
│
├── server.js
├── package.json
├── package-lock.json
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone <your-github-repository-url>
```

### 2. Open the project

```bash
cd PriceScout
```

### 3. Install dependencies

```bash
npm install
```

### 4. Start the server

```bash
npm start
```

Or, if the project uses Nodemon:

```bash
npm run dev
```

### 5. Open in browser

```text
http://localhost:3000
```

---

## 🧪 Example Search

Try searching:

```text
laptop
```

or:

```text
smartphone
```

or:

```text
headphones
```

or:

```text
tv
```

or:

```text
fridge
```

The backend recognizes related keywords and returns the relevant category.

---

## 🔄 Data Flow

```text
User enters search
        ↓
JavaScript frontend
        ↓
REST API request
        ↓
Express.js server
        ↓
Search / synonym matching
        ↓
Product catalogue
        ↓
JSON response
        ↓
Frontend displays products
```

---

## 🎯 Project Objective

The main objective of Price Scout is to simplify online product research by bringing useful product comparison information into a single interface.

Instead of manually searching multiple shopping websites, users can search for a product, view its details, and access the corresponding shopping links.

---

## 🔮 Future Improvements

Possible future enhancements include:

* Live price fetching from shopping platforms
* Price history tracking
* Price-drop notifications
* Advanced product filters
* Product sorting by price/rating
* Wishlist functionality
* Secure password hashing
* JWT-based authentication
* MongoDB database integration
* Admin dashboard
* Cloud deployment
* Mobile application

---

## 👨‍💻 Project Type

**Full-Stack Web Application**

### Frontend

```text
HTML + CSS + JavaScript
```

### Backend

```text
Node.js + Express.js
```

### Communication

```text
REST APIs + JSON
```

---

## 📌 Disclaimer

Product information and shopping links used in this project are provided for demonstration and educational purposes. Prices, availability, ratings, and other product information may change on external shopping platforms.

---

## ⭐ Project Highlights

* Full-stack implementation
* REST API development
* Product search and filtering
* Keyword/synonym matching
* User authentication
* Order management
* Product comparison interface
* Amazon and Flipkart shopping links
* Express.js backend
* JSON-based API communication
