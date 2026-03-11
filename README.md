# NeuroCards - AI-Powered Flashcard Generator

A modern, AI-powered flashcard application that helps students learn smarter using spaced repetition algorithms.

## Features

âœ¨ **AI Flashcard Generation** - Paste text and let AI create perfect study cards
ðŸŽ¯ **Spaced Repetition** - Proven memory technique for efficient learning
ðŸ“Š **Progress Tracking** - Monitor your study streak and mastery
ðŸŒ™ **Dark/Light Mode** - Easy on the eyes, day or night
ðŸ“± **Mobile Responsive** - Study anywhere, on any device
ðŸ’¾ **Local Storage** - Your data stays private in your browser

## Quick Start

### Option 1: Open Locally

1. Download all files to a folder
2. Open `index.html` in your web browser
3. Start creating flashcards!

### Option 2: Deploy to Hosting

Deploy to any static hosting service:

**Netlify (Recommended)**
```bash
# Install Netlify CLI
npm install -g netlify-cli

# Deploy
netlify deploy --prod
```

**Vercel**
```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
vercel --prod
```

**GitHub Pages**
1. Create a new repository on GitHub
2. Upload all files
3. Go to Settings â†’ Pages â†’ Source â†’ main branch
4. Your app will be live at `https://yourusername.github.io/neurocards`

**Simple HTTP Server (For Testing)**
```bash
# Python 3
python -m http.server 8000

# Node.js
npx http-server -p 8000

# Then open http://localhost:8000
```

## How to Use

### 1. Get Started
- Click "Sign Up" (demo login - no real authentication required)
- Enter any email to access the dashboard

### 2. Create Flashcards

**AI Generation** (Requires Anthropic API Key)
- Get your API key from [console.anthropic.com](https://console.anthropic.com/)
- Paste your study material (notes, textbook content, etc.)
- Click "Generate Flashcards"
- AI will automatically create question-answer pairs

**Manual Entry**
- Click "Manual Entry" tab
- Add questions and answers manually
- Perfect for quick deck creation

### 3. Study with Spaced Repetition
- Click "Study Now" on any deck
- Review each flashcard
- Rate difficulty: Easy, Medium, or Hard
- Cards are scheduled for optimal review timing:
  - **Hard** â†’ Review in 30 minutes
  - **Medium** â†’ Review tomorrow
  - **Easy** â†’ Review in 3 days

### 4. Track Progress
- View total flashcards created
- Monitor your study streak
- Check mastery rate
- See daily study progress

## File Structure

```
neurocards/
â”œâ”€â”€ index.html          # Main HTML structure
â”œâ”€â”€ styles.css          # Complete styling with themes
â”œâ”€â”€ app.js              # All JavaScript logic
â””â”€â”€ README.md           # This file
```

## Technologies Used

- **HTML5** - Semantic structure
- **CSS3** - Modern styling with CSS variables
- **Vanilla JavaScript** - No dependencies!
- **Anthropic Claude API** - AI flashcard generation
- **LocalStorage** - Client-side data persistence

## API Integration

This app uses the Anthropic Claude API for AI generation. You need:

1. Sign up at [console.anthropic.com](https://console.anthropic.com/)
2. Get your API key
3. Enter it in the "Create Flashcards" page
4. API key is stored locally (never sent to any server except Anthropic)

**Note:** Manual flashcard entry works without an API key.

## Browser Support

- âœ… Chrome/Edge (latest)
- âœ… Firefox (latest)
- âœ… Safari (latest)
- âœ… Mobile browsers

## Customization

### Change Colors
Edit CSS variables in `styles.css`:
```css
:root {
    --accent-primary: #6366f1;  /* Primary brand color */
    --accent-secondary: #4f46e5; /* Secondary brand color */
    /* ... more variables */
}
```

### Add More Card Types
Modify the `generateWithAI()` function in `app.js` to support:
- Multiple choice questions
- Fill-in-the-blank
- True/false questions
- Image-based cards

### Customize Spaced Repetition
Adjust intervals in `rateCard()` function in `app.js`:
```javascript
case 'easy':
    card.nextReview = new Date(now.getTime() + 3 * 24 * 60 * 60 * 1000); // 3 days
```

## Limitations (Prototype)

This is a **front-end only prototype**. Production features that need backend:

- âŒ Real user authentication
- âŒ Cloud data sync
- âŒ PDF text extraction
- âŒ Image OCR
- âŒ Payment processing
- âŒ Multi-device sync
- âŒ Sharing decks with friends

**For these features**, you'll need to build a backend API with:
- Database (PostgreSQL/MongoDB)
- Authentication service (Auth0/Firebase)
- File processing (PDF parser, OCR service)
- Payment integration (Stripe)

## Next Steps to Production

To turn this into a full production app:

1. **Backend Setup**
   - Node.js/Express or Python/FastAPI
   - PostgreSQL database
   - User authentication (JWT)
   - File upload handling

2. **Advanced Features**
   - PDF processing (pdf-parse, PyPDF2)
   - Image OCR (Tesseract, Google Vision)
   - Cloud storage (AWS S3)
   - Email notifications

3. **Mobile Apps**
   - React Native (iOS/Android)
   - Flutter alternative
   - Progressive Web App (PWA)

4. **Monetization**
   - Stripe subscription integration
   - Free tier limits
   - Premium features gate

## License

This is a prototype/demo application. Feel free to use and modify for your projects!

## Support

For issues or questions about deployment, check:
- [Netlify Docs](https://docs.netlify.com/)
- [Vercel Docs](https://vercel.com/docs)
- [Anthropic API Docs](https://docs.anthropic.com/)

---

**Built with â¤ï¸ for students who want to learn smarter, not harder.**
