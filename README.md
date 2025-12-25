# Grant Intelligence Hub - AI Agent Website

A comprehensive AI-powered grant management platform that helps organizations discover, write, and manage successful grant applications.

## 🚀 Features

- **AI-Powered Grant Discovery**: Intelligent matching algorithm for funding opportunities
- **Smart Proposal Writing**: AI writing assistant trained on successful applications
- **Deadline Management**: Automated tracking and reminders
- **Compliance Monitoring**: Real-time requirement verification
- **Success Analytics**: Performance tracking and optimization
- **Interactive AI Chat**: Real-time assistance and guidance

## 🎯 Target Audience

- Nonprofits and NGOs
- Educational Institutions
- Small Businesses and Startups
- Government Organizations
- Research Institutions

## 🛠️ Technology Stack

- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **Styling**: Custom CSS with CSS Grid and Flexbox
- **Icons**: Font Awesome 6.4.0
- **Fonts**: Google Fonts (Inter, Playfair Display)
- **Responsive**: Mobile-first design approach

## 📁 Project Structure

```
website/
├── index.html              # Main website file
├── README.md              # This file
├── DEPLOYMENT.md          # Deployment instructions
├── package.json           # Node.js dependencies (optional)
├── .gitignore            # Git ignore file
└── assets/               # Additional assets (if needed)
    ├── images/
    ├── css/
    └── js/
```

## 🚀 Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/grant-intelligence-hub.git
   cd grant-intelligence-hub
   ```

2. **Open locally**
   ```bash
   # Simple HTTP server
   python -m http.server 8000
   # or
   npx serve .
   ```

3. **Visit** `http://localhost:8000`

## 🌐 Deployment Options

### Option 1: GitHub Pages (Free)
1. Push code to GitHub repository
2. Go to Settings > Pages
3. Select source branch (main)
4. Your site will be available at `https://yourusername.github.io/grant-intelligence-hub`

### Option 2: Vercel (Recommended)
1. Connect GitHub repository to Vercel
2. Automatic deployments on every push
3. Custom domain support
4. Global CDN

### Option 3: Netlify
1. Drag and drop the website folder
2. Or connect GitHub repository
3. Automatic deployments
4. Form handling capabilities

## 🎨 Customization

### Colors
The website uses CSS custom properties for easy theming:

```css
:root {
    --primary-color: #4F46E5;
    --secondary-color: #7C3AED;
    --accent-color: #06B6D4;
    /* ... more variables */
}
```

### AI Chat Responses
Modify the `predefinedResponses` object in the JavaScript section to customize AI responses:

```javascript
'grant opportunities': {
    keywords: ['grant', 'opportunity', 'funding'],
    response: 'Your custom response here...'
}
```

## 📱 Responsive Design

The website is fully responsive and optimized for:
- Desktop (1200px+)
- Tablet (768px - 1199px)
- Mobile (320px - 767px)

## 🔧 Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## 📈 Performance

- Optimized images and assets
- Minimal external dependencies
- Efficient CSS and JavaScript
- Fast loading times

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📞 Support

For questions or support:
- Email: support@grantintelligencehub.com
- Documentation: [Link to docs]
- Issues: GitHub Issues tab

## 🔄 Updates

- v1.0.0 - Initial release with core AI chat functionality
- v1.1.0 - Enhanced responsive design
- v1.2.0 - Improved AI responses and animations

---

Built with ❤️ for the grant-seeking community