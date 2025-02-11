# 🛒 Product API

A **RESTful API** for managing products, built with **Node.js, Express, and MongoDB**.

## 📌 Features
✔ Fetch all products  
✔ Retrieve a single product by ID  
✔ Create a new product  
✔ Update an existing product  
✔ Delete a product  

---

## 🚀 Getting Started

### **1. Clone the Repository**
```sh
git clone <repo-url>
cd <repo-folder>
```

### **2. Install Dependencies**
```sh
npm install
```

### **3. Set Up Environment Variables**
Create a `.env` file in the root directory and add:
```env
MONGO_URI=your_mongodb_connection_string
PORT=4000
```

### **4. Start the Server**
Run the API server with:
```sh
npm start
```
or with **nodemon** (for development):
```sh
npm run dev
```
The API will run on **http://localhost:4000** (or your specified `PORT`).

---

## 📡 API Endpoints

### **1. Get All Products**
```http
GET /api/products
```
🔹 **Response:**  
```json
[
  {
    "_id": "65a12345bc678d90efg12345",
    "name": "Laptop",
    "price": 999.99,
    "category": "Electronics"
  }
]
```

---

### **2. Get a Single Product**
```http
GET /api/products/:id
```
🔹 **Response:**
```json
{
  "_id": "65a12345bc678d90efg12345",
  "name": "Laptop",
  "price": 999.99,
  "category": "Electronics"
}
```

---

### **3. Create a Product**
```http
POST /api/products
```
🔹 **Request Body (JSON):**
```json
{
  "name": "Smartphone",
  "price": 599.99,
  "category": "Electronics"
}
```
🔹 **Response:**
```json
{
  "_id": "65b67890bc123d45efg67890",
  "name": "Smartphone",
  "price": 599.99,
  "category": "Electronics"
}
```

---

### **4. Update a Product**
```http
PUT /api/products/:id
```
🔹 **Request Body (JSON):**
```json
{
  "price": 549.99
}
```
🔹 **Response:**
```json
{
  "_id": "65b67890bc123d45efg67890",
  "name": "Smartphone",
  "price": 549.99,
  "category": "Electronics"
}
```

---

### **5. Delete a Product**
```http
DELETE /api/products/:id
```
🔹 **Response:**
```json
{
  "message": "Product deleted successfully"
}
```

---

## 🛠 Technologies Used
- **Node.js** + **Express.js** (Server)
- **MongoDB** + **Mongoose** (Database)
- **dotenv** (Environment variables)
- **nodemon** (Development)

---

## 📜 Project Structure
```
/project-root
│── /models
│   ├── product.model.js    # Mongoose schema for Product
│
│── /routes
│   ├── product.route.js    # Defines product-related API routes
│
│── /controllers
│   ├── product.controller.js  # Handles request logic for products
│
│── .env                     # Environment variables (MongoDB URI, PORT)
│── index.js                  # Main server entry point
│── package.json              # Project dependencies
```

