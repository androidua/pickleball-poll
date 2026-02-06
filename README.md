# Pickleball Venue Poll - Centralized Version

An interactive poll with **centralized vote storage** so you can see all votes from all users in real-time!

## Question
**What matters most when choosing a pickleball venue?**

Options:
- Court quality
- Location convenience
- Price or affordability
- Social atmosphere
- Coaching or events availability

---

## ⚠️ Important: Setup Required

This version uses **JSONBin.io** as a free backend to store votes centrally. You need to set this up once before deploying.

---

## Quick Setup Guide (5 minutes)

### Step 1: Create a Free JSONBin Account

1. Go to **https://jsonbin.io**
2. Click "Sign Up" and create a free account
3. After signing in, go to your dashboard

### Step 2: Create a Bin (Your Database)

1. In the JSONBin dashboard, click **"Create Bin"**
2. Paste this JSON data:
```json
{
  "Court quality": 0,
  "Location convenience": 0,
  "Price or affordability": 0,
  "Social atmosphere": 0,
  "Coaching or events availability": 0
}
```
3. Click **"Create"**
4. **Copy the Bin ID** (looks like: `67abc123def456789`)

### Step 3: Get Your API Key

1. In JSONBin dashboard, click on your profile (top right)
2. Go to **"API Keys"**
3. Click **"Create Access Key"**
4. Give it a name like "Pickleball Poll"
5. **Copy the API key** (starts with `$2a$10$...`)

### Step 4: Configure Your Credentials

1. Open **config.js** in a text editor
2. Replace the placeholder values with your actual credentials:
```javascript
const CONFIG = {
    JSONBIN_API_KEY: 'YOUR_API_KEY_HERE',
    BIN_ID: 'YOUR_BIN_ID_HERE'
};
```
3. Replace `YOUR_API_KEY_HERE` with your actual API key
4. Replace `YOUR_BIN_ID_HERE` with your actual Bin ID

**Example:**
```javascript
const CONFIG = {
    JSONBIN_API_KEY: '$2a$10$abcdefghijklmnopqrstuvwxyz123456',
    BIN_ID: '67abc123def456789'
};
```

> **Note:** Both `index.html` and `results.html` load credentials from `config.js`, so you only need to edit this one file. A `config.example.js` template is also provided for reference.

---

## Deploy to GitHub Pages

### Step 1: Create Repository
1. Go to **github.com** and create a new repository
2. Name it `pickleball-poll` (or anything you like)
3. Make it **public**

### Step 2: Upload Files
1. Upload **index.html**, **results.html**, and **config.js** to your repository
2. You can drag and drop them on GitHub

### Step 3: Enable GitHub Pages
1. Go to repository **Settings**
2. Click **"Pages"** in the left sidebar
3. Under "Source", select **"main"** branch
4. Select **"/ (root)"** folder
5. Click **"Save"**

### Step 4: Access Your Poll
After a few minutes, your poll will be live at:
- **Poll URL**: `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`
- **Results URL**: `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/results.html`

Share the poll URL with your friends!

---

## How It Works Now

✅ **Centralized Storage**: All votes are stored in JSONBin's cloud  
✅ **Real-time Updates**: Results page auto-refreshes every 10 seconds  
✅ **Everyone Sees Same Results**: Your friends' votes appear for everyone  
✅ **Persistent**: Votes are saved even if you close your browser  
✅ **Free**: JSONBin free tier includes 10,000 requests/month (plenty for a poll)

---

## Features

- Clean, modern interface
- Real-time vote counting with centralized storage
- Visual bar charts showing percentages
- Responsive design (works on mobile)
- Auto-refreshing results page
- Reset functionality to clear all votes

---

## Troubleshooting

**Problem: "Configuration Required" warning shows**
- Make sure you've replaced `YOUR_API_KEY_HERE` and `YOUR_BIN_ID_HERE` in `config.js`

**Problem: Votes not showing up**
- Check browser console for errors (F12 → Console tab)
- Verify your API key and Bin ID are correct
- Make sure you created the bin with the correct initial JSON structure

**Problem: "Failed to fetch votes" error**
- Your API key might be incorrect
- Your Bin ID might be incorrect
- Check that the bin exists in your JSONBin dashboard

---

## Security Note

Your API key is visible in the HTML source code. For a public poll this is acceptable since:
- The free tier has rate limits that prevent abuse
- You can regenerate the API key anytime if needed
- The worst case is someone resets your poll data

For production apps with sensitive data, use a backend server to hide API keys.

---

## Alternative: Using Your Own Backend

If you want even more control, you can replace the JSONBin code with:
- **Firebase Realtime Database** (Google)
- **Supabase** (open source)
- **Your own API** (Node.js, Python, etc.)

The code structure is simple to modify - just update the `getVotes()` and `updateVotes()` functions.

---

## Files

- `index.html` - Main poll page where users vote
- `results.html` - Results page showing live vote distribution
- `config.js` - Your JSONBin credentials (edit this file)
- `config.example.js` - Template with placeholder values for reference
- `README.md` - This file with setup instructions

---

## Questions?

If you run into issues:
1. Double-check your API key and Bin ID are copied correctly in `config.js`
2. Make sure `config.js` is uploaded to your repository alongside the HTML files
3. Verify the bin was created with the correct JSON structure
4. Check browser console for error messages

Enjoy your poll! 🏓
