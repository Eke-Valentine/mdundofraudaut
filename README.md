# 🚀 Mdundo Fraud Detection - GitHub Ready

All files you need to deploy fraud detection on GitHub with automation at 6 AM EAT daily.

## 📁 Files Included

```
github_fraud/
├── .github/workflows/
│   └── daily-fraud-check-accurate.yml      ← GitHub Actions workflow
├── scripts/
│   └── accurate_fraud_detection.py         ← Main fraud detection script
├── requirements.txt                        ← Python dependencies
├── README.md                               ← This file
├── DEPLOYMENT_GUIDE.md                     ← Setup instructions
├── SETUP_ACCURATE_FRAUD_DETECTION.md       ← Detailed guide
└── OPTION_B_IMPLEMENTATION.md              ← Quick reference
```

## ⚡ Quick Start (Copy & Paste)

### 1. Copy all files to your GitHub repo
```bash
# Navigate to your repo
cd ~/Documents/YOUR-REPO-NAME

# Copy from github_fraud folder
cp -r "/Users/valentineeke/Documents/Claude/Projects/Mdundo analysis/github_fraud/"* .
```

### 2. Add GitHub Secrets
GitHub Repo → Settings → Secrets and variables → Actions

Add these 3:
```
SLACK_WEBHOOK = https://hooks.slack.com/services/...
SPOTIFY_CLIENT_ID = your_spotify_id
SPOTIFY_CLIENT_SECRET = your_spotify_secret
```

### 3. Commit & Push
```bash
git add .
git commit -m "Add fraud detection automation"
git push
```

### 4. Test It
- GitHub repo → Actions
- Click "Daily Mdundo Fraud Detection - Accurate Data"
- Click "Run workflow"
- Check #fraud-automation in Slack for results

## ✅ What Happens

**After deployment:**
- ✅ Runs automatically every day at 6 AM EAT
- ✅ Scrapes real Mdundo chart data
- ✅ Checks Spotify for artist verification
- ✅ Calculates fraud scores (0-100)
- ✅ Posts results to #fraud-automation channel
- ✅ Saves results to JSON file

## 🔍 Fraud Detection Checks

- Not on Spotify? +20 points
- Low Spotify followers? +15 points
- Top rank but 0 listeners? +35 points
- Suspicious name keywords? +25 points
- Too many numbers in name? +15 points

**Risk Levels:**
- 🔴 CRITICAL (60+) - Remove from charts
- 🟠 HIGH (40-59) - Request verification
- 🟡 MEDIUM (20-39) - Monitor
- ✅ CLEAN (0) - Legitimate

## 📊 Expected Output

You'll see Slack messages like:

```
🚨 NIGERIA - Fraud Alert
Analyzed: 87 | Flagged: 12
───────────────────────────

🔴 #3 Suspicious Artist
   Score: 85/100 | Risk: CRITICAL
   Mdundo Listeners: 0
   • Not found on Spotify
   • Top 5 rank but 0 monthly listeners
```

## 🛠️ Need Help?

Check `DEPLOYMENT_GUIDE.md` for troubleshooting.
