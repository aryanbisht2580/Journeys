# Journeys - E-commerce Shoe Store

A full-stack e-commerce platform specializing in branded shoes from top brands like Adidas, Nike, New Balance, Puma, and more. The application features separate admin and user panels with comprehensive functionality for managing products, orders, and user accounts.

## 🚀 Features

### User Panel
- **Product Browsing**: Browse and search through a wide collection of branded shoes
- **User Authentication**: Secure login/registration with JWT tokens
- **Shopping Cart**: Add products to cart and manage quantities
- **Secure Payments**: Integrated Razorpay payment gateway for secure transactions
- **Order Tracking**: Track order status from placement to delivery
- **Password Recovery**: Email-based password reset using NodeMailer
- **Responsive Design**: Optimized for all screen sizes and devices

### Admin Panel
- **Product Management**: Add, update, and delete products
- **Inventory Control**: Manage stock levels and product details
- **Order Management**: View all orders and update order status (Order Placed → Shipped → Delivered)
- **Order Tracking**: Monitor order progression and customer details
- **Dashboard Analytics**: Overview of sales, orders, and inventory

### General Features
- **Pagination**: Efficient data loading with pagination
- **Responsive Design**: Mobile-first approach with cross-device compatibility
- **Secure Authentication**: JWT-based authentication system
- **Real-time Updates**: Dynamic status updates for orders and inventory

## 🛠️ Tech Stack

### Frontend
- **React.js** - Component-based UI library
- **Tailwind CSS** - Utility-first CSS framework
- **Ant Design (AntD)** - Enterprise-class UI design language
- **Redux** - State management for complex application state

### Backend
- **Node.js** - JavaScript runtime environment
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database for data storage
- **JWT (jsonwebtoken)** - Secure authentication tokens
- **Crypto** - Built-in Node.js module for encryption
- **NodeMailer** - Email sending functionality
- **Razorpay** - Payment gateway integration

## 📦 Installation & Setup

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or cloud instance)
- npm or yarn package manager

### Clone Repository
```bash
git clone https://github.com/aryanbisht2580/Journeys.git
cd journeys
```

### Backend Setup
```bash
cd backend
npm install

# Create .env file with the following variables:
# PORT=5000
# MONGODB_URI=your_mongodb_connection_string
# JWT_SECRET=your_jwt_secret_key
# RAZORPAY_KEY_ID=your_razorpay_key_id
# RAZORPAY_KEY_SECRET=your_razorpay_key_secret
# EMAIL_USER=your_email_for_nodemailer
# EMAIL_PASS=your_email_password

npm start
```

### Frontend Setup
```bash
cd frontend
npm install
npm start
```

The application will be available at:
- Frontend: `http://localhost:3000`
- Backend API: `http://localhost:5000`

## 🔐 Environment Variables

Create a `.env` file in the backend directory:

```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/journeys
JWT_SECRET=your_super_secret_jwt_key
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_password
```

## 🏗️ Project Structure

```
journeys/
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── redux/
│   │   ├── utils/
│   │   └── App.js
│   ├── public/
│   └── package.json
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── utils/
│   └── server.js
└── README.md
```

## 🔧 API Endpoints

### User Authentication & Management
- `POST /api/users/register` - User registration
- `POST /api/users/login` - User login
- `GET /api/users/dashboard` - User dashboard (Protected)
- `POST /api/users/adminDashboard` - Admin dashboard (Admin only)
- `POST /api/users/getForgetPassword` - Send password reset email
- `POST /api/users/setForgetPassword` - Reset password with token
- `POST /api/users/updateUserProfile` - Update user profile (Protected)

### Products
- `POST /api/products/createProduct` - Create new product (Admin only)
- `PUT /api/products/updateProduct/:pid` - Update product by ID (Admin only)
- `GET /api/products/getAllProducts` - Get all products with pagination
- `GET /api/products/getProduct/:slug` - Get single product by slug
- `GET /api/products/getPhoto/:pid` - Get product photo by ID
- `DELETE /api/products/deleteProduct/:pid` - Delete product by ID
- `GET /api/products/getAllBrands` - Get all available brands
- `POST /api/products/getFilterProduct/:page` - Get filtered products with pagination
- `GET /api/products/getproductCount` - Get total product count

### Categories
- `POST /api/categories/createCategory` - Create new category (Admin only)
- `PUT /api/categories/updateCategory/:id` - Update category by ID (Admin only)
- `GET /api/categories/getCategories` - Get all categories
- `GET /api/categories/getCategory/:slug` - Get single category by slug
- `DELETE /api/categories/deleteCategory/:id` - Delete category by ID (Admin only)

### Shopping Cart
- `GET /api/cart/` - Get user's cart items (Protected)
- `POST /api/cart/add` - Add item to cart (Protected)
- `POST /api/cart/remove` - Remove item from cart (Protected)
- `POST /api/cart/updateQuantity` - Update item quantity in cart (Protected)
- `POST /api/cart/getNumber` - Get cart items count
- `GET /api/cart/deleteAll` - Clear entire cart (Protected)

### Orders
- `GET /api/orders/` - Get user's orders (Protected)
- `GET /api/orders/allOrders` - Get all orders (Admin only)
- `POST /api/orders/changeStatus` - Update order status (Admin only)

## 👥 User Roles

### Customer
- Browse and purchase products
- Manage personal account
- Track order status
- Write product reviews

### Admin
- Full product management
- Order management and status updates
- User management
- Analytics and reporting

## 🎨 UI Components

The application uses a combination of custom components and Ant Design components:
- Responsive navigation with mobile menu
- Product cards with image galleries
- Shopping cart with quantity controls
- Order status timeline
- Admin dashboard with tables and forms
- Payment integration interface

## 🔒 Security Features

- JWT token-based authentication
- Password encryption using crypto module
- Protected API routes
- Input validation and sanitization
- Secure payment processing with Razorpay

## 📸 Screenshots

### 🏠 Home Page
<img width="1470" alt="image" src="https://github.com/user-attachments/assets/c06ccb7c-6069-4c63-a618-60bf7bb7035e" />

### 👟 Products Page
<img width="1468" alt="image" src="https://github.com/user-attachments/assets/6eca399c-c9bf-4436-b234-4cdb184a7d19" />

### 🗂️ Products Detial Page
<img width="1470" alt="image" src="https://github.com/user-attachments/assets/cf4a48e7-3852-450c-8fcf-4b183e086e69" />

### 🗂️ Cart Page
<img width="1466" alt="image" src="https://github.com/user-attachments/assets/abae98e0-2cae-4802-ac8a-e746f36652e9" />

### 🛠️ Admin Panel
<img width="1464" alt="image" src="https://github.com/user-attachments/assets/4d024f91-af7d-41de-baaf-95c4d2f82202" />


### 📦 Orders Management
<img width="1463" alt="image" src="https://github.com/user-attachments/assets/67c1b43e-e43d-4a41-bfa2-43e576ef69b1" />

### 💳 Payment Integration (Razorpay)
<img width="1464" alt="image" src="https://github.com/user-attachments/assets/af9d1e5d-c841-45a2-87d5-87d59e4ab44f" />


## 📱 Responsive Design

The application is fully responsive and optimized for:
- Desktop (1024px and above)
- Tablet (768px - 1023px)
- Mobile (320px - 767px)

## 🚀 Deployment

### Frontend Deployment
Build the React application:
```bash
cd frontend
npm run build
```

### Backend Deployment
Ensure all environment variables are configured for production environment.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📞 Contact

For any queries or support, please contact aryanbisht2580@gmail.com

---

**Happy Shopping with Journeys! 👟**
