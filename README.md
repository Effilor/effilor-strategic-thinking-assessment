# Strategic Thinking Quotient Assessment

A professional assessment tool to measure organizational strategic thinking capability across three pillars: Thinking Far, Thinking Big, and Thinking Different.

## 🎯 Assessment Overview

- **18 Questions** across 3 strategic pillars
- **Immediate results display** with detailed breakdown
- **Optional email capture** for full report delivery
- **Mobile-responsive design** matching Effilor brand
- **Single-file HTML** - no build process required

## 📁 Project Structure

```
strategic-thinking-assessment/
├── index.html              # Main assessment application (single file)
├── effilor-logo.jpg        # Effilor logo (must be uploaded)
├── api/
│   └── send-email.js       # Vercel serverless function for SendGrid
└── README.md               # This file
```

## 🚀 Deployment Instructions

### Step 1: Create GitHub Repository

1. Go to https://github.com/new
2. Repository name: `strategic-thinking-assessment` (or your preferred name)
3. Set to **Public** or **Private**
4. **Do NOT** initialize with README, .gitignore, or license
5. Click **Create repository**

### Step 2: Push Code to GitHub

Open your terminal and run:

```bash
cd /path/to/your/local/folder
git init
git add .
git commit -m "Initial commit: Strategic Thinking Quotient Assessment"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/strategic-thinking-assessment.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your actual GitHub username.

### Step 3: Deploy to Vercel

1. Go to https://vercel.com/new
2. Click **Import Git Repository**
3. Select your `strategic-thinking-assessment` repository
4. Configure project:
   - **Framework Preset**: Other (leave as is)
   - **Root Directory**: ./
   - **Build Command**: (leave empty)
   - **Output Directory**: (leave empty)
5. Click **Deploy**

### Step 4: Configure Environment Variables

**CRITICAL - Do this before testing!**

1. In your Vercel dashboard, go to your project
2. Click **Settings** → **Environment Variables**
3. Add the following variable:

```
Name:  SENDGRID_API_KEY
Value: [Your SendGrid API Key]
```

4. Click **Save**
5. Go back to **Deployments** tab
6. Click the **⋯** menu on the latest deployment
7. Click **Redeploy** (this applies the environment variable)

### Step 5: Get Your SendGrid API Key

If you don't have a SendGrid API key:

1. Go to https://sendgrid.com/
2. Sign up or log in
3. Go to **Settings** → **API Keys**
4. Click **Create API Key**
5. Name it "Effilor Strategic Thinking Assessment"
6. Select **Full Access** permission
7. Click **Create & View**
8. **IMPORTANT**: Copy the API key immediately (you won't see it again)
9. Paste this key into Vercel's environment variable

### Step 6: Verify Deployment

Your assessment will be live at:
```
https://your-project-name.vercel.app
```

Or with custom domain (optional):
```
https://strategic-thinking.effilor.com
```

## ✅ Testing Checklist

Before declaring success, test ALL of these:

### Desktop Testing
- [ ] Assessment loads correctly on desktop browser (Chrome, Firefox, Safari)
- [ ] Logo displays correctly on welcome screen (centered, large)
- [ ] Logo displays correctly on question screens (top, small)
- [ ] All 18 questions display properly
- [ ] Progress bar updates correctly
- [ ] Can navigate back to previous questions
- [ ] Answer selection works (button highlights when selected)
- [ ] Scoring calculates correctly (manual spot check)

### Mobile Testing
- [ ] Assessment loads correctly on mobile device
- [ ] All text is readable (no horizontal scrolling needed)
- [ ] Buttons are tap-friendly (not too small)
- [ ] Logo scales appropriately on mobile
- [ ] Forms are easy to fill out on mobile

### Results Screen Testing
- [ ] Overall score displays correctly
- [ ] Score level (Transactional/Emerging/Strategic) is accurate
- [ ] Pillar breakdown bar charts render correctly
- [ ] Top Strength and Priority Area identify correctly
- [ ] Detailed feedback displays for all three pillars
- [ ] CTA box for email capture displays

### Email Capture Testing
- [ ] Email form displays when "Get Your Full Report" is clicked
- [ ] All form fields are present (Name, Email, Company, Role, Phone)
- [ ] Form validation works (try submitting empty form)
- [ ] Phone field is optional (can submit without it)

### Email Delivery Testing
- [ ] Lead notification email sends to shankar.ramamurthy@effilor.com
- [ ] Check INBOX for email
- [ ] Check SPAM folder for email
- [ ] Email contains all user data (name, email, company, role, phone)
- [ ] Email contains total score and level
- [ ] Email contains pillar breakdown scores
- [ ] Email contains all 18 question responses

### Thank You Screen Testing
- [ ] Thank you screen displays after form submission
- [ ] User's name displays correctly
- [ ] User's email displays correctly
- [ ] Appropriate messaging about 24-hour delivery

### Error Handling Testing
- [ ] Test with invalid email address
- [ ] Test form submission with network disconnected
- [ ] Verify error messages display appropriately

## 🔧 Environment Variables

Required environment variable in Vercel:

```
SENDGRID_API_KEY=SG.xxxxxxxxxxxxxxxxxxxxx
```

This must be set in Vercel project settings for emails to work.

## 📧 Email Configuration

Lead notifications are sent to:
- **Recipient**: shankar.ramamurthy@effilor.com
- **From**: shankar.ramamurthy@effilor.com
- **Subject**: "New Strategic Thinking Assessment - [Name] ([Company])"

Email includes:
- Contact information (name, email, company, role, phone)
- Overall score and level
- Pillar-by-pillar breakdown
- All 18 detailed question responses
- JSON format data for easy parsing

## 🎨 Branding

- **Primary Color**: #6B3D7A (Effilor Purple)
- **Logo**: Embedded as base64 in HTML
- **Typography**: System fonts via Tailwind CSS
- **Design**: Matches Growth Mindset Assessment style

## 🔄 Making Updates

To update the assessment after deployment:

1. Edit files locally
2. Commit changes: `git add . && git commit -m "Description of changes"`
3. Push to GitHub: `git push`
4. Vercel automatically redeploys (usually takes 30-60 seconds)

## 📊 Score Ranges

- **67-90 points**: Strategic Thinking
- **43-66 points**: Emerging Strategic Thinking
- **18-42 points**: Transactional Thinking

Each pillar (6 questions × 5 points max) = 30 points maximum

## 🛠️ Troubleshooting

### Emails not sending?

1. Check Vercel environment variables are set correctly
2. Verify SendGrid API key is valid (test in SendGrid dashboard)
3. Check Vercel Function Logs for errors:
   - Go to your Vercel project
   - Click **Deployments** → latest deployment
   - Click **Functions** tab
   - Check `/api/send-email` logs

### Assessment not loading?

1. Check browser console for JavaScript errors (F12 → Console)
2. Verify `index.html` deployed correctly
3. Try hard refresh (Ctrl+F5 or Cmd+Shift+R)

### Styling looks broken?

1. Ensure Tailwind CDN loads: Check Network tab for `cdn.tailwindcss.com`
2. Try different browser
3. Clear browser cache

## 📞 Support

For issues or questions:
- Contact: shankar.ramamurthy@effilor.com
- Review Vercel deployment logs
- Check GitHub repository for latest code

## 📝 License

© 2025 Effilor Consulting Services. All rights reserved.
