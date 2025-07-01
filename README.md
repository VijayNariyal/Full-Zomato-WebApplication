# FoodHub - Zomato Clone

A full-stack restaurant discovery and food ordering platform built with React, Node.js, Express, and MongoDB.

## 🚀 Features

### User Features
- **Authentication**: Secure user registration and login with JWT
- **Restaurant Discovery**: Browse restaurants by city, cuisine, and rating
- **Restaurant Details**: View menus, reviews, and restaurant information
- **Shopping Cart**: Add items to cart and place orders
- **Order History**: Track past orders and their status
- **Reviews & Ratings**: Leave reviews and ratings for restaurants

### Admin Features
- **Restaurant Management**: Add, update, and delete restaurants
- **Order Management**: View and update order status
- **Featured Restaurants**: Mark restaurants as featured
- **Analytics Dashboard**: View orders and restaurant statistics

## 🛠️ Tech Stack

### Frontend
- **React 18** with TypeScript
- **React Router** for navigation
- **Tailwind CSS** for styling
- **Axios** for API calls
- **React Hot Toast** for notifications
- **Framer Motion** for animations

### Backend
- **Node.js** with Express.js
- **MongoDB** with Mongoose ODM
- **JWT** for authentication
- **bcrypt** for password hashing
- **Express Rate Limit** for API protection
- **Helmet** for security headers

## 📦 Installation & Setup

### Prerequisites
- Node.js (v16 or higher)
- MongoDB (local or MongoDB Atlas)
- npm or yarn

### 1. Clone the repository
```bash
git clone <repository-url>
cd foodhub
```

### 2. Install dependencies
```bash
# Install root dependencies
npm install

# Install frontend dependencies
cd frontend
npm install

# Install backend dependencies
cd ../backend
npm install
```

### 3. Set up Environment Variables
```bash
# In the backend directory, create .env file
cp .env.example .env

# Edit .env with your MongoDB connection string and JWT secret
MONGODB_URI=mongodb://localhost:27017/foodhub
JWT_SECRET=your-super-secret-jwt-key-here
PORT=5000
```

### 4. Seed the Database
```bash
# From the backend directory
npm run seed
```

This will create sample restaurants and demo user accounts:
- **User**: user@demo.com / password
- **Admin**: admin@demo.com / password

### 5. Start the Application
```bash
# From the root directory, start both frontend and backend
npm run dev

# Or start them separately:
# Backend (from backend directory)
npm run dev

# Frontend (from frontend directory)
npm run dev
```

The application will be available at:
- **Frontend**: http://localhost:5173
- **Backend**: http://localhost:5000

## 🗂️ Project Structure

```
foodhub/
├── frontend/                 # React frontend
│   ├── src/
│   │   ├── components/      # Reusable components
│   │   ├── pages/          # Page components
│   │   ├── context/        # React context providers
│   │   ├── types/          # TypeScript type definitions
│   │   └── utils/          # Utility functions
│   ├── public/             # Static assets
│   └── package.json
├── backend/                  # Node.js backend
│   ├── models/             # Mongoose models
│   ├── routes/             # API routes
│   ├── middleware/         # Custom middleware
│   ├── scripts/            # Database scripts
│   └── package.json
├── package.json             # Root package.json
└── README.md
```

## 🔧 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/me` - Get current user

### Restaurants
- `GET /api/restaurants` - Get all restaurants (with filters)
- `GET /api/restaurants/:id` - Get restaurant details
- `POST /api/restaurants` - Create restaurant (Admin only)
- `PUT /api/restaurants/:id` - Update restaurant (Admin only)
- `DELETE /api/restaurants/:id` - Delete restaurant (Admin only)

### Reviews
- `POST /api/reviews` - Create review
- `GET /api/reviews/restaurant/:id` - Get restaurant reviews

### Orders
- `POST /api/orders` - Create order
- `GET /api/orders` - Get user orders
- `PUT /api/orders/:id` - Update order status (Admin only)

### Admin
- `GET /api/admin/orders` - Get all orders (Admin only)

## 🎨 Design Features

- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Modern UI**: Clean, professional interface with smooth animations
- **Color System**: Carefully chosen color palette with proper contrast
- **Typography**: Inter font family with proper hierarchy
- **Micro-interactions**: Hover effects and smooth transitions
- **Loading States**: Skeleton loading and progress indicators

## 🔒 Security Features

- **JWT Authentication**: Secure token-based authentication
- **Password Hashing**: bcrypt for secure password storage
- **Rate Limiting**: Protection against API abuse
- **Input Validation**: Server-side validation for all inputs
- **CORS Configuration**: Proper cross-origin resource sharing
- **Security Headers**: Helmet.js for security headers

## 🚀 Deployment

### Frontend (Netlify/Vercel)
1. Build the frontend: `cd frontend && npm run build`
2. Deploy the `dist` folder to your preferred platform

### Backend (Railway/Render/Digital Ocean)
1. Set environment variables on your platform
2. Deploy the backend directory
3. Update frontend API URLs to point to your deployed backend

### Database
- Use MongoDB Atlas for production database
- Update `MONGODB_URI` in environment variables

## 📱 Mobile Responsiveness

The application is fully responsive with breakpoints at:
- **Mobile**: < 640px
- **Tablet**: 640px - 1024px  
- **Desktop**: > 1024px

## 🧪 Testing

```bash
# Run frontend tests
cd frontend
npm test

# Run backend tests
cd backend
npm test
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit changes: `git commit -am 'Add feature'`
4. Push to branch: `git push origin feature-name`
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Images from [Pexels](https://pexels.com) for restaurant and food photos
- Icons from [Lucide React](https://lucide.dev)
- Fonts from [Google Fonts](https://fonts.google.com)

## 📞 Support

For support, email support@foodhub.com or create an issue in the repository.