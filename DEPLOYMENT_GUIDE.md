# 🚀 GitHub Fraud Detection - Deployment Guide

## 📁 Folder Structure

```
github_fraud/
├── .github/workflows/
│   └── daily-fraud-check-accurate.yml    ← GitHub Actions workflow
├── scripts/
│   └── accurate_fraud_detection.py       ← Main fraud detection script
├── SETUP_ACCURATE_FRAUD_DETECTION.md     ← Detailed setup guide
├── OPTION_B_IMPLEMENTATION.md            ← Quick reference
└── DEPLOYMENT_GUIDE.md                   ← This file
```

---

## 🎯 Quick Deployment (10 minutes)

### 1. Get Spotify Credentials (5 min)
- Visit https://developer.spotify.com
- Create a free account and app
- Copy: `Client ID` and `Client Secret`

### 2. Get Slack Webhook (3 min)
- In Slack: **Settings & administration** → **Manage apps**
- Search for **Incoming Webhooks**
- Create new webhook for **#fraud-automation**
- Copy the webhook URL

### 3. Copy Files to Your GitHub Repo (2 min)

Option A: Copy manually
```bash
# Copy these 4 items from github_fraud/ folder to your GitHub repo:
1. .github/workflows/daily-fraud-check-accurate.yml  → your_repo/.github/workflows/
2. scripts/accurate_fraud_detection.py              → your_repo/scripts/
3. SETUP_ACCURATE_FRAUD_DETECTION.md               → your_repo/root/
4. OPTION_B_IMPLEMENTATION.md                      → your_repo/root/
```

Option B: One command
```bash
cp -r github_fraud/* /path/to/your/repo/
```

### 4. Add GitHub Secrets (2 min)

GitHub Repo → **Settings** → **Secrets and variables** → **Actions**

Add 3 secrets:
```
SLACK_WEBHOOK = https://hooks.slack.com/services/...
SPOTIFY_CLIENT_ID = your_spotify_id
SPOTIFY_CLIENT_SECRET = your_spotify_secret
```

---

## ✅ Test It

1. Push to GitHub
2. Go to GitHub repo → **Actions**
3. Select **Daily Mdundo Fraud Detection - Accurate Data**
4. Click **Run workflow**
5. Check **#fraud-automation** in Slack for results

---

## 🔄 Automation

After testing, the workflow runs **automatically every day at 6 AM EAT** with:
- Real Mdundo chart data
- Actual monthly listener counts
- Spotify verification
- Accurate fraud scoring
- Slack alerts with results

---

## 📞 Troubleshooting

**Issue:** No data in Slack  
**Fix:** Check SPOTIFY_CLIENT_ID and SPOTIFY_CLIENT_SECRET are set correctly

**Issue:** Wrong listener counts  
**Fix:** Mdundo may have changed HTML structure - update BeautifulSoup selectors in script

**Issue:** Webhook error  
**Fix:** Get fresh webhook URL from Slack app settings

---

**Ready? Start with Step 1 above →**
