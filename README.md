# Dhruthi's Empire Dashboard 👑

**"I swore my loyalty to me, myself and I" - Fate of Ophelia**

A personal dashboard for tracking goals, business progress, and building an empire.

---

## 🚀 Quick Start

### Login Credentials:
- **Username:** `dhruthi`
- **Password:** `empire2027`

---

## 📦 What's Inside

### 1. **Personal Dashboard** (`dhruthi-dashboard.html`)
Your command center featuring:
- ✅ Life Goals Tracker
- ✅ Business Roadmap with Milestones
- ✅ Interactive Calendar
- ✅ Smart Reminders
- ✅ AI Assistant (Built-in chatbot)
- ✅ Current Stats
- ✅ Learning Progress Tracker

### 2. **Complete Roadmap** (`DHRUTHI-EMPIRE-ROADMAP.md`)
Your detailed plan from today to age 27:
- Phase-by-phase breakdown (Feb 2026 - 2030)
- Monthly action items
- Financial projections
- Week-by-week tasks
- Mindset reminders
- Progress tracking

---

## 🌐 Deploy to GitHub Pages

### Step 1: Create GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the **+** button (top right) → **New repository**
3. Name it: `dhruthi-empire-dashboard` (or any name you like)
4. Make it **Public**
5. Click **Create repository**

### Step 2: Upload Your Files

**Option A: Upload via GitHub Web Interface (Easiest)**

1. On your new repository page, click **Add file** → **Upload files**
2. Drag and drop these files:
   - `dhruthi-dashboard.html`
   - `DHRUTHI-EMPIRE-ROADMAP.md`
   - `README.md` (this file)
3. Click **Commit changes**

**Option B: Using Git Command Line**

```bash
# Navigate to your folder
cd /path/to/your/files

# Initialize git
git init

# Add files
git add .

# Commit
git commit -m "Initial commit - Empire Dashboard"

# Add remote (replace YOUR-USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR-USERNAME/dhruthi-empire-dashboard.git

# Push
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. In your repository, click **Settings** (top menu)
2. Scroll down to **Pages** (left sidebar)
3. Under **Source**, select **main** branch
4. Click **Save**
5. Wait 1-2 minutes

### Step 4: Rename HTML File (Important!)

For the website to work at the root URL, you need to rename your file:

1. In your repository, click on `dhruthi-dashboard.html`
2. Click the pencil icon (Edit)
3. Change the filename from `dhruthi-dashboard.html` to `index.html`
4. Click **Commit changes**

### Step 5: Access Your Dashboard

Your dashboard will be live at:
```
https://YOUR-USERNAME.github.io/dhruthi-empire-dashboard/
```

Replace `YOUR-USERNAME` with your actual GitHub username.

---

## 🎨 Customize Your Dashboard

### Change Login Credentials

Edit the `index.html` file and find this section (around line 673):

```javascript
const VALID_CREDENTIALS = {
    username: 'dhruthi',
    password: 'empire2027'
};
```

Change the username and password to whatever you want.

### Update Your Information

You can edit any text in the HTML file:
- Goals
- Milestones
- Reminders
- Stats

Just open `index.html` in any text editor and modify the content.

### Change Colors/Theme

Find the `:root` CSS variables at the top of the file (around line 10):

```css
:root {
    --primary-dark: #0a0a0f;
    --secondary-dark: #1a1a2e;
    --accent-gold: #d4af37;
    --accent-rose: #e6b8a2;
    /* ... */
}
```

Change these hex color codes to customize your theme.

---

## 🤖 Adding a Real AI Agent

The current AI assistant has basic pre-programmed responses. To add a real AI (like Claude):

### Option 1: Use Anthropic API (Advanced)

1. Sign up at [Anthropic Console](https://console.anthropic.com)
2. Get an API key
3. Replace the `getAIResponse()` function with:

```javascript
async function getAIResponse(message) {
    const response = await fetch("https://api.anthropic.com/v1/messages", {
        method: "POST",
        headers: {
            "Content-Type": "application/json",
            "x-api-key": "YOUR_API_KEY_HERE",
            "anthropic-version": "2023-06-01"
        },
        body: JSON.stringify({
            model: "claude-sonnet-4-20250514",
            max_tokens: 1000,
            messages: [{
                role: "user",
                content: `You are Dhruthi's personal AI assistant. You know she's 23, working at KPMG, doing an MBA, planning to start a business, and preparing for LLB. Be supportive, motivating, and help her stay on track. User message: ${message}`
            }]
        })
    });
    
    const data = await response.json();
    return data.content[0].text;
}
```

**Note:** Never commit API keys to public repositories! Use environment variables or a backend service.

### Option 2: Use a Free AI Chat Widget

Services like:
- **Voiceflow** (free tier available)
- **Chatbase** (free tier available)
- **Botpress** (open source)

These can be embedded as iframes or widgets.

---

## 📱 Mobile Friendly

The dashboard is fully responsive and works great on:
- 📱 Mobile phones
- 💻 Tablets
- 🖥️ Desktop computers

---

## ✨ Features

### Calendar
- Interactive month navigation
- Highlights today
- Shows events (dots on dates)
- Click days to add events (you can extend this)

### Reminders
- Pre-loaded with your weekly tasks
- Click "Add Reminder" to create new ones
- Marks urgent items

### AI Assistant
- Built-in chat interface
- Responds to keywords like:
  - "help" - Shows what it can do
  - "business" - Explains your business roadmap
  - "motivation" - Gives you encouragement
  - "scared" - Addresses fears
  - "timeline" - Reviews your timeline

### Stats Dashboard
- Age counter
- Target year for LLB
- Capital goal
- Target age

---

## 🔄 Updating Your Dashboard

Whenever you want to update your dashboard:

1. Edit the `index.html` file locally or on GitHub
2. Commit the changes
3. GitHub Pages will automatically update in 1-2 minutes

---

## 📊 Tracking Your Progress

Use your dashboard to:
1. **Weekly:** Update progress bars on your goals
2. **Monthly:** Add new milestones and achievements
3. **Daily:** Check reminders and chat with AI assistant

---

## 🎯 This Week's Tasks

As per your roadmap, here's what you need to do THIS WEEK:

1. ✅ **Follow 20 Instagram accounts** (fashion/business niche)
2. ✅ **Message 3 vendors** for catalogs and pricing
3. ✅ **30 minutes daily learning** about your market

Update your dashboard's reminders section to track these!

---

## 💪 Motivation

Every time you log in, you'll see:
> "I swore my loyalty to me, myself and I"

This is YOUR empire. YOUR dashboard. YOUR journey.

Use it daily.
Update it weekly.
Review it monthly.

By age 27, you'll look back at this and be amazed at what you built.

---

## 📞 Need Help?

If you get stuck with GitHub or deployment:
1. Check [GitHub Pages Documentation](https://docs.github.com/en/pages)
2. Watch a YouTube tutorial on "How to deploy to GitHub Pages"
3. Ask in GitHub Community forums

---

## 🚀 Next Steps

1. ✅ Deploy to GitHub Pages
2. ✅ Bookmark your dashboard URL
3. ✅ Set it as your browser homepage
4. ✅ Log in daily
5. ✅ Complete this week's 3 tasks
6. ✅ Update progress bars as you go
7. ✅ Build your empire, one day at a time

---

**Remember:**

The empire doesn't build itself overnight.
But it DOES build.
One week at a time.
Starting now.

Let's go. 👑

---

*Fate of Ophelia - February 2026*
