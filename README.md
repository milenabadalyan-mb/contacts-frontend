# 🎨 Contacts Frontend

A modern single-page contact management application with authentication. Built with vanilla JavaScript and inspired by Picsart's vibrant color palette.

## ✨ Features

- **Authentication**: User registration & login with JWT tokens
- **Contact Management**: Add and view contacts (name, email, phone)
- **Modern UI**: Dark theme with electric purple, magenta, and cyan accents
- **Responsive**: Adapts to any screen size
- **No Dependencies**: Pure HTML/CSS/JavaScript

## 🚀 Quick Start

1. **Open the app**:
   ```bash
   open index.html
   ```
   Or serve it with a local server:
   ```bash
   python3 -m http.server 8000
   ```

2. **Configure backend** (default: `http://localhost:5050`):
   
   If your backend runs on a different port, edit line 145 in `index.html`:
   ```javascript
   const baseUrl = 'http://localhost:5050';
   ```

## 📡 API Endpoints

The frontend expects the following backend endpoints:

### Authentication
- `POST /api/auth/register`
  - Body: `{ username, password }`
  
- `POST /api/auth/login`
  - Body: `{ username, password }`
  - Response: `{ token }`

### Contacts
- `GET /api/contacts`
  - Headers: `x-auth-token: <jwt-token>`
  
- `POST /api/contacts`
  - Headers: `x-auth-token: <jwt-token>`
  - Body: `{ name, email?, phone? }`

## 🎨 Design System

### Color Palette
| Color | Hex | Usage |
|-------|-----|-------|
| Electric Purple | `#8a2be2` | Primary accent |
| Magenta | `#ff4fd8` | Secondary accent |
| Cyan | `#00c2ff` | Tertiary accent |
| Dark Navy | `#0f0f1a` | Background |
| White | `#ffffff` | Text |

### Typography
- **Font**: Inter, system-ui, Segoe UI, Arial, sans-serif
- **Border Radius**: 14px (cards), 10-12px (components)

## 🏗️ Architecture

```
contacts-frontend/
├── index.html          # Complete SPA (HTML + CSS + JS)
└── README.md          # This file
```

### Key Features
- **State Management**: Token stored in localStorage
- **API Communication**: Fetch API with JSON
- **Security**: XSS prevention with HTML escaping
- **Error Handling**: Toast notifications & 401 auto-logout

## 🔧 Tech Stack

- Pure HTML/CSS/JavaScript (zero dependencies)
- CSS Custom Properties for theming
- LocalStorage for token persistence
- Fetch API for HTTP requests

## 🐛 Troubleshooting

| Issue | Solution |
|-------|----------|
| Can't login/register | Ensure backend is running on correct port |
| Contacts not loading | Verify token is valid, check CORS on backend |
| Toast not showing | Check browser console for errors |

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

---

Inspired by Picsart colors!
