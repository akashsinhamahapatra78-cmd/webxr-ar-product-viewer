# WebXR AR Product Viewer

> A production-ready Full-Stack WebXR AR Product Viewer web app that lets shoppers place true-to-scale 3D product models in their real world using React/Three.js frontend and Node.js + MongoDB backend.

## Overview

WebXR AR Product Viewer is a cutting-edge e-commerce solution that leverages WebXR technology to enable customers to visualize products in their own space before making a purchase. Using Augmented Reality (AR) capabilities, shoppers can place true-to-scale 3D product models directly in their environment through their device's camera.

## Features

- 🎯 **WebXR AR Integration**: Full WebXR support for placing 3D products in real-world environments
- 📱 **Cross-Platform**: Works on mobile devices, tablets, and AR-enabled browsers
- 🎨 **3D Product Models**: High-quality, optimized 3D models with realistic rendering
- 🛒 **E-commerce Integration**: Seamless integration with product catalogs and shopping features
- 🌐 **Real-time Sync**: Real-time product data synchronization between frontend and backend
- 🔐 **Secure Backend**: Production-ready Node.js backend with MongoDB database
- ⚡ **Performance Optimized**: Optimized for fast loading and smooth AR experience
- 📊 **Analytics**: Track user interactions and AR session data

## Tech Stack

### Frontend
- **React** - UI framework and state management
- **Three.js** - 3D graphics rendering
- **WebXR API** - Augmented Reality capabilities
- **TypeScript** - Type-safe JavaScript development
- **Tailwind CSS** - Utility-first CSS framework
- **React Router** - Client-side routing
- **Axios** - HTTP client for API communication

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web framework and middleware
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **JWT** - Authentication and authorization
- **Multer** - File upload handling
- **Cors** - Cross-Origin Resource Sharing
- **Dotenv** - Environment variable management

### DevOps & Tools
- **Git & GitHub** - Version control
- **Docker** - Containerization (optional)
- **Jest** - Testing framework
- **ESLint** - Code linting
- **Prettier** - Code formatting

## Project Structure

```
webxr-ar-product-viewer/
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   │   ├── ARViewer.tsx
│   │   │   ├── ProductCard.tsx
│   │   │   └── Navigation.tsx
│   │   ├── pages/
│   │   │   ├── Home.tsx
│   │   │   ├── ProductDetail.tsx
│   │   │   └── AR.tsx
│   │   ├── services/
│   │   │   ├── api.ts
│   │   │   └── webxr.ts
│   │   ├── hooks/
│   │   │   └── useAR.ts
│   │   ├── types/
│   │   │   └── index.ts
│   │   ├── App.tsx
│   │   └── index.tsx
│   ├── package.json
│   └── tsconfig.json
│
├── backend/
│   ├── src/
│   │   ├── routes/
│   │   │   ├── products.ts
│   │   │   ├── auth.ts
│   │   │   └── users.ts
│   │   ├── controllers/
│   │   │   ├── productController.ts
│   │   │   ├── authController.ts
│   │   │   └── userController.ts
│   │   ├── models/
│   │   │   ├── Product.ts
│   │   │   ├── User.ts
│   │   │   └── ARSession.ts
│   │   ├── middleware/
│   │   │   ├── auth.ts
│   │   │   └── errorHandler.ts
│   │   ├── config/
│   │   │   └── database.ts
│   │   ├── server.ts
│   │   └── index.ts
│   ├── .env.example
│   ├── package.json
│   └── tsconfig.json
│
├── .gitignore
├── README.md
└── LICENSE
```

## Getting Started

### Prerequisites
- Node.js (v16 or higher)
- npm or yarn
- MongoDB (local or cloud instance)
- A device or browser with WebXR support

### Installation

#### Backend Setup

```bash
cd backend
npm install
cp .env.example .env
# Update .env with your MongoDB connection string and API keys
npm run dev
```

#### Frontend Setup

```bash
cd frontend
npm install
npm start
```

The app will open at `http://localhost:3000`

## API Endpoints

### Products
- `GET /api/products` - Get all products
- `GET /api/products/:id` - Get product by ID
- `POST /api/products` - Create new product (admin only)
- `PUT /api/products/:id` - Update product (admin only)
- `DELETE /api/products/:id` - Delete product (admin only)

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout
- `POST /api/auth/refresh` - Refresh authentication token

### AR Sessions
- `POST /api/ar-sessions` - Create AR session
- `GET /api/ar-sessions/:id` - Get AR session details
- `PUT /api/ar-sessions/:id` - Update AR session

## Usage

1. **Browse Products**: Users can view available products in the catalog
2. **View in AR**: Click the "View in AR" button to activate the AR viewer
3. **Place Product**: Use device camera to place the 3D model in your environment
4. **Interact**: Rotate, scale, and move the model to see how it fits
5. **Purchase**: Add items to cart and proceed to checkout

## Environment Variables

Create a `.env` file in the `backend` directory:

```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/webxr-ar-product-viewer
JWT_SECRET=your_jwt_secret_key
JWT_EXPIRE=7d
NODE_ENV=development
CORS_ORIGIN=http://localhost:3000
```

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, email support@example.com or open an issue on GitHub.

## Roadmap

- [ ] Advanced AR gesture controls
- [ ] Multi-product AR scenes
- [ ] AR product sharing via social media
- [ ] Voice-activated AR controls
- [ ] Analytics dashboard for sellers
- [ ] Progressive Web App (PWA) support
- [ ] Real-time multiplayer AR viewing

## Authors

- Your Name - *Initial work*

## Acknowledgments

- WebXR Community
- Three.js Documentation
- React Documentation
