# Ramadan Kareem Website 🌙

A light, playful website that asks "Are you going to say Ramadan Kareem to me?" with Yes and No buttons.

## Features

- **Yes button**: Shows a popup with a thank you message and the smiling cat image
- **No button**: Runs away when you try to click it! But if you somehow catch it, shows a cute cat with stickers and "I am so happy to make you smile and made your day"
- **Light background music**: Click the music button (🔇) in the bottom-right to play peaceful ambient music
- **Tracking**: Optional email notifications when someone opens the page or clicks buttons

## How to Run

1. Open `index.html` in your browser (double-click or drag into browser)
2. Or use a local server: `python -m http.server 8000` then visit http://localhost:8000

## Email / Tracking Notifications

To get notified when someone opens the link or clicks buttons:

### Option 1: Formspree (Recommended - Free)

1. Go to [formspree.io](https://formspree.io) and create a free account
2. Create a new form - you'll get an endpoint like `https://formspree.io/f/xxxxxxxx`
3. Open `index.html` and find the config section (around line 211):
   - Replace `YOUR_FORM_ID` with your form ID (the `xxxxxxxx` part)
   - Set `TRACKING_ENABLED = true`
4. You'll receive an email for each: page visit, Yes click, and No click

### Option 2: webhook.site (Quick Testing)

1. Go to [webhook.site](https://webhook.site) - you'll get a unique URL
2. In `index.html`, set `FORMSPREE_ENDPOINT = 'https://webhook.site/YOUR-ID'`
3. Set `TRACKING_ENABLED = true`
4. View all requests in real-time on the webhook.site page

## Custom Music

To use your own music instead of the default track: create `assets/audio/background.mp3` and update the `<audio>` source in `index.html` to point to it.

## Deploy Online

- **GitHub Pages**: Push to a repo, enable Pages in Settings
- **Netlify**: Drag the folder to [netlify.com/drop](https://app.netlify.com/drop)
- **Vercel**: `npx vercel` in the project folder

---

Ramadan Kareem! 💚
