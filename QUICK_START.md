# 🚀 QUICK START: Deploy in 10 Minutes

Follow these steps exactly to get your Strategic Thinking Assessment live.

## Prerequisites Checklist
- [ ] GitHub account (free)
- [ ] Vercel account (free - sign up with GitHub)
- [ ] SendGrid account (free tier works)

---

## Step 1: Download Files (1 minute)

You should have received these files:
```
strategic-thinking-assessment/
├── index.html
├── effilor-logo.jpg (IMPORTANT: Must upload this!)
├── api/
│   └── send-email.js
├── README.md
├── .gitignore
└── QUICK_START.md (this file)
```

---

## Step 2: Create GitHub Repository (2 minutes)

1. Go to: https://github.com/new
2. Repository name: `strategic-thinking-assessment`
3. Make it **Private** (recommended) or Public
4. **DO NOT** check any initialization options
5. Click **Create repository**
6. Keep this page open - you'll need it

---

## Step 3: Upload Files to GitHub (3 minutes)

### Option A: Using GitHub Web Interface (Easier)
1. In your new repository, click **uploading an existing file**
2. Drag and drop ALL files from your folder
3. Scroll down, add commit message: "Initial commit"
4. Click **Commit changes**

### Option B: Using Command Line (If you're comfortable with Git)
```bash
cd /path/to/strategic-thinking-assessment
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/strategic-thinking-assessment.git
git push -u origin main
```

---

## Step 4: Deploy to Vercel (2 minutes)

1. Go to: https://vercel.com/new
2. Sign in with GitHub (if not already)
3. Click **Import Git Repository**
4. Find `strategic-thinking-assessment` and click **Import**
5. Leave all settings as default
6. Click **Deploy**
7. Wait 30-60 seconds for deployment to complete
8. **IMPORTANT**: Do NOT click "Visit" yet - we need to add the email API key first!

---

## Step 5: Get SendGrid API Key (5 minutes)

### If you don't have SendGrid account yet:
1. Go to: https://sendgrid.com/
2. Click **Start for Free**
3. Sign up (free tier is fine)
4. Verify your email address

### Get your API Key:
1. Log into SendGrid
2. Click **Settings** (left sidebar)
3. Click **API Keys**
4. Click **Create API Key**
5. Name: `Effilor Strategic Thinking`
6. Permission: **Full Access**
7. Click **Create & View**
8. **COPY THE KEY NOW** (you'll only see it once!)
9. Keep it somewhere safe temporarily

---

## Step 6: Add API Key to Vercel (2 minutes)

1. In Vercel, go to your project dashboard
2. Click **Settings** tab (top menu)
3. Click **Environment Variables** (left sidebar)
4. Add new variable:
   - **Name**: `SENDGRID_API_KEY`
   - **Value**: Paste your SendGrid API key (starts with `SG.`)
   - **Environment**: Check all three (Production, Preview, Development)
5. Click **Save**
6. Go to **Deployments** tab
7. Find your latest deployment (top of list)
8. Click the **⋯** (three dots) menu
9. Click **Redeploy**
10. Wait 30 seconds for redeploy to finish

---

## Step 7: Test Your Assessment! (5 minutes)

Your assessment is now live at: `https://your-project-name.vercel.app`

### Testing Checklist:
1. **Open the assessment** - Does it load?
2. **Check the logo** - Does Effilor logo appear?
3. **Take the assessment** - Answer all 18 questions
4. **View results** - Do scores calculate correctly?
5. **Request full report** - Fill in the email form
6. **Check your email** - Did it arrive at shankar.ramamurthy@effilor.com?
   - Check INBOX
   - Check SPAM folder
7. **Verify email contents** - Does it have all the data?

---

## 🎉 You're Done!

Your assessment is live and working!

### Your URLs:
- **Live Assessment**: https://your-project-name.vercel.app
- **Vercel Dashboard**: https://vercel.com/dashboard
- **GitHub Repo**: https://github.com/YOUR_USERNAME/strategic-thinking-assessment

---

## 🔧 Common Issues & Fixes

### "Email not sending"
**Fix**: 
1. Check Vercel → Settings → Environment Variables
2. Make sure `SENDGRID_API_KEY` is set
3. Redeploy after adding it (Step 6, steps 6-10)

### "Assessment not loading"
**Fix**: 
1. Check your Vercel deployment status (should be green checkmark)
2. Try hard refresh: Ctrl+F5 (Windows) or Cmd+Shift+R (Mac)
3. Try different browser

### "Styling looks broken"
**Fix**: 
1. Check internet connection (needs Tailwind CDN)
2. Try hard refresh
3. Check browser console (F12) for errors

### "Can't find my API key"
**Fix**: 
1. Create a new one in SendGrid (you can have multiple)
2. Delete the old one if needed

---

## 📞 Need Help?

Contact shankar.ramamurthy@effilor.com with:
- Screenshot of the issue
- Link to your Vercel deployment
- What step you're on

---

## 🔄 Making Changes Later

1. Edit files locally
2. Upload to GitHub (drag & drop or git push)
3. Vercel automatically redeploys in 30-60 seconds

---

## 🎯 Next Steps (Optional)

### Add Custom Domain:
1. Vercel → Settings → Domains
2. Add: strategic-thinking.effilor.com
3. Follow DNS instructions
4. Wait for propagation (5-30 minutes)

### Monitor Responses:
- Check shankar.ramamurthy@effilor.com inbox regularly
- Create a folder/label for assessment emails
- Track leads in your CRM

---

**Good luck! Your Strategic Thinking Quotient Assessment is ready to generate leads! 🚀**
