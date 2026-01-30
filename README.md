# contacts-frontend

A single-page contact management app with authentication. Built with vanilla JavaScript.

Features

- User registration & login (JWT authentication)
- Add and view contacts (name, email, phone)
- Modern dark UI with Picsart-inspired colors
- Responsive design

## Quick Start

1. Open `index.html` in your browser
2. Default backend: `http://localhost:5050`
3. To change backend port, edit line 145 in `index.html`:
   const baseUrl = 'http://localhost:5050';

## API Requirements
The frontend expects these endpoints:
- POST /api/auth/register - Register user
- POST /api/auth/login - Login (returns JWT token)
- GET /api/contacts - Get contacts (requires x-auth-token header)
- POST /api/contacts - Create contact (requires x-auth-token header)

## Color Palette
- Electric Purple: #8a2be2
- Magenta: #ff4fd8
- Cyan: #00c2ff
- Dark Background: #0f0f1a

Made with 💜 inspired by Picsart colors
