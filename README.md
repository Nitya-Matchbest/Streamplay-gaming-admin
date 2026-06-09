# 📝 StreamPlay Admin Panel

Admin panel for managing StreamPlay blog posts - separated from the backend.

---

## 🚀 Quick Start

### Development (Local Testing)

```bash
# Option 1: Using npx (no installation)
npx http-server -p 3001

# Option 2: Using Live Server (VS Code Extension)
# Right-click on index.html → Open with Live Server
```

Then open: **http://localhost:3001**

---

## 📂 Project Structure

```
streamplay-admin/
├── index.html          # Main admin page
├── css/
│   └── admin.css      # All styles
├── js/
│   └── admin.js       # All JavaScript & API logic
├── README.md          # This file
└── package.json       # NPM scripts (optional)
```

---

## 🔧 Configuration

### API URL Configuration

Edit `js/admin.js` to set your backend URL:

```javascript
// For Development (localhost)
const API_BASE = 'http://localhost:5000';

// For Production (after deployment)
const API_BASE = 'https://your-backend-url.com';
```

**Auto-detection is already configured:**
- Localhost → Uses `http://localhost:5000`
- Deployed → Update the URL in `js/admin.js` line 3

---

## 🌐 Deployment

### Deploy to Vercel (Recommended)

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel
```

**Or use Vercel Web UI:**
1. Go to https://vercel.com
2. Import your Git repository
3. Set root directory: `streamplay-admin`
4. Deploy!

### Deploy to Netlify

1. Drag and drop the `streamplay-admin` folder to https://app.netlify.com/drop
2. Done!

### Custom Domain Setup

After deployment:
- Vercel: `admin.yourdomain.com`
- Update API URL in `js/admin.js` before deployment

---

## ✨ Features

- ✅ Create blog posts
- ✅ Upload images (5MB max)
- ✅ Add multiple content sections
- ✅ Tag management
- ✅ Character counters
- ✅ Image preview
- ✅ Form validation
- ✅ Responsive design

---

## 📋 Requirements

- Backend API running at `http://localhost:5000` (development)
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection (for API calls)

---

## 🐛 Troubleshooting

### Admin panel loads but can't create blogs

**Issue:** API connection failed

**Solution:**
1. Check if backend is running: `http://localhost:5000/api/health`
2. Verify API URL in `js/admin.js`
3. Check browser console (F12) for CORS errors

### Image upload fails

**Issue:** Upload endpoint not found

**Solution:**
1. Ensure backend has upload route: `POST /api/upload`
2. Check backend is restarted after adding upload functionality
3. Verify CORS is enabled in backend

### Styles not loading

**Issue:** CSS path incorrect

**Solution:**
1. Ensure `css/admin.css` exists
2. Check `index.html` has: `<link rel="stylesheet" href="css/admin.css">`

---

## 🔗 Related Projects

- **Backend API:** `streamplay-backend`
- **Frontend Website:** `streamplay-frontend`

---

## 📝 Notes

- This is a standalone admin panel (no backend files)
- Connects to backend API for all operations
- Can be deployed independently
- No database - pure frontend

---

## 🎯 Next Steps

1. ✅ Admin panel separated from backend
2. ⏳ Deploy admin to Vercel
3. ⏳ Deploy backend to Render
4. ⏳ Update API URLs in production
5. ⏳ Set up custom domain

---

**Happy Blogging! 🚀**
