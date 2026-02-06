# Pickleball Venue Poll

An interactive poll to gather feedback on what matters most when choosing a pickleball venue.

## Question
**What matters most when choosing a pickleball venue?**

Options:
- Court quality
- Location convenience
- Price or affordability
- Social atmosphere
- Coaching or events availability

## How to Deploy to GitHub Pages

1. **Create a new repository on GitHub**
   - Go to github.com and create a new repository
   - Name it something like `pickleball-poll`
   - Make it public

2. **Upload these files**
   - Upload `index.html` and `results.html` to your repository
   - You can drag and drop them directly on GitHub

3. **Enable GitHub Pages**
   - Go to your repository Settings
   - Scroll down to "Pages" section
   - Under "Source", select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Click Save

4. **Access your poll**
   - After a few minutes, your poll will be live at:
   - `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`
   - Share this URL with people to vote!

5. **View results**
   - You can view results at:
   - `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/results.html`

## Features

- Clean, modern interface
- Real-time vote counting
- Visual bar charts showing percentages
- Responsive design (works on mobile)
- Results page with auto-refresh
- Reset functionality for starting new polls

## How It Works

The poll uses browser localStorage to store votes. This means:
- Votes are stored locally in each user's browser
- Results are aggregated across all users who visit the page
- Data persists between page visits
- No backend server required

## Note

Since this uses localStorage, votes are stored client-side. For a production poll with many users, consider using a backend service like Firebase, Supabase, or a custom API to store votes centrally.

## Files

- `index.html` - Main poll page where users vote
- `results.html` - Results page showing vote distribution
- `README.md` - This file
