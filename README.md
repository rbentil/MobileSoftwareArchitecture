# MobileSoftwareArchitecture

# Web-Based E-commerce Platform for Laptops

An advanced e-commerce platform designed for selling laptops, leveraging microservices architecture for enhanced scalability, modularity, and maintainability.

## 🚀 Features
- **Multi-Vendor Support:** Allows multiple vendors to list and manage their products.
- **Authentication & Authorization:** Secure user management with JWT-based authentication.
- **Product Management:** CRUD operations for products with categories, stock tracking, and search capabilities.
- **Order Processing:** Efficient cart management, checkout, and order tracking.
- **Microservices Architecture:** Modular services for authentication, products, orders, and API gateway.
- **Real-Time Communication:** Integrated RabbitMQ for inter-service messaging.

## 🛠️ Tech Stack
- **Frontend:** React.js, Tailwind CSS
- **Backend:** Node.js, Express.js
- **Database:** MongoDB, PostgreSQL
- **Message Broker:** RabbitMQ
- **Authentication:** JWT (JSON Web Tokens)
- **API Gateway:** Express-based Proxy

## 🗂️ Microservices Overview
1. **Authentication Service**
   - Handles user registration, login, and token management.
   - Database: `auth_database`
2. **Product Service**
   - Manages product listings, categories, and inventory.
   - Database: `products`
3. **Order Service**
   - Processes orders, handles payments, and manages order statuses.
   - Database: `orderDB`
4. **API Gateway**
   - Routes requests to the appropriate microservices and handles cross-origin requests.

## 📦 Installation
```bash
# Clone the repository
git clone https://github.com/your-username/laptop-ecommerce.git
cd laptop-ecommerce

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env

# Run services
docker-compose up --build
```

## 📝 API Documentation
### 1. Authentication API
- **Base Path:** `/auth`
- **POST /register:** Registers a new user.
- **POST /login:** Authenticates a user.
- **POST /refresh-token:** Refreshes JWT tokens.
- **POST /logout:** Logs out the user.

### 2. Product API
- **Base Path:** `/products`
- **GET /:** Fetch all products.
- **POST /:** Add a new product.
- **GET /:id:** Fetch product by ID.
- **PUT /:id:** Update product details.
- **DELETE /:id:** Delete a product.

### 3. Order API
- **Base Path:** `/orders`
- **POST /:** Create a new order.
- **GET /:** Retrieve all orders.
- **PATCH /:id:** Update order status.
- **DELETE /:id:** Cancel an order.

## 📊 Database Schema
- **Users:** `id`, `username`, `email`, `password`, `role`
- **Products:** `id`, `name`, `price`, `description`, `category`, `stock`, `image`
- **Orders:** `id`, `user_id`, `products`, `total`, `status`, `created_at`

## 🔗 Deployment
- **Frontend:** [GitHub Repository](#)
- **Backend:** [GitHub Repository](#)
- **Live Demo:** [Hosted Application](#)

## 🤝 Contributing
1. Fork the repository
2. Create a new branch (`git checkout -b feature-branch`)
3. Commit your changes (`git commit -m 'Add new feature'`)
4. Push to the branch (`git push origin feature-branch`)
5. Open a Pull Request

## 📄 License
This project is licensed under the MIT License.

## 📧 Contact
- **Project Maintainers:** [Insert Names]
- **Email:** [Insert Contact Email]
- **LinkedIn:** [Insert LinkedIn Profile]

