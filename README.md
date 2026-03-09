# Cloudery — Digital Products Online Store

Cloudery is a full-stack web application for buying and downloading digital products. Users can browse, purchase, and access digital content, while administrators manage the product catalog, categories, and orders.

Built solo from scratch using Laravel (REST API backend) and ReactJS (frontend).

## Features

### Users
- Register and log in with secure token-based authentication (Laravel Sanctum)
- Browse products by category with search, filtering, and sorting
- Preview partial content before purchase (watermarked images, partial documents)
- Purchase products instantly or via cart
- Access and download full content after purchase
- View order history and purchased products in profile
- Live currency conversion — RSD, EUR, USD (ExchangeRate API)
- Password reset flow

### Administrators
- Manage products and categories (create, edit, delete)
- View all user orders
- Sales analytics dashboard with charts by category (Recharts)
- Dedicated admin interface

## Tech Stack

**Frontend:** ReactJS, Axios, Bootstrap, Recharts  
**Backend:** Laravel 10, Laravel Sanctum, PHP  
**Database:** MySQL — 6-table relational schema with joins, transactions, and triggers  
**External APIs:** ExchangeRate API (live currency conversion)

## Project Structure

```
Cloudery/
├── backend/    # Laravel RESTful API
└── frontend/   # ReactJS application
```

## Getting Started

### Prerequisites
- PHP 8.x, Composer
- Node.js, npm
- MySQL

### Backend Setup

```bash
cd backend
composer install
cp .env.example .env
php artisan key:generate
```

Configure your MySQL connection in `.env`:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=digitalproducts_db
DB_USERNAME=root
DB_PASSWORD=
```

Run migrations and seed the database:

```bash
php artisan migrate --seed
php artisan serve
```

### Frontend Setup

```bash
cd frontend
npm install
npm start
```

## Test Credentials

**Admin account:**  
Email: `admin@gmail.com`  
Password: `admin123`

**User account:** Register a new account manually.
