# 🚀 Automated Commit Bot

A minimalist, high-performance GitHub Action designed to automate commits to your repository on a cron schedule. Perfect for maintaining a consistent contribution profile and testing CI/CD pipelines.

![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)

## ✨ Features

- **Automated Scheduling**: Runs twice daily (00:00 & 12:00 UTC) via GitHub Actions.
- **Dynamic Content**: Fetches a fresh inspirational quote or "Daily Thought" for every commit.
- **Personalized Graph**: Configured to use your personal GitHub email to ensure every automated commit counts as a "green" contribution square.
- **Zero Configuration**: Just fork it, enable Actions, and you're good to go.

## 🛠️ How It Works

The bot uses the `auto-commit.yml` workflow to:
1.  **Trigger**: Fire off on a schedule or manual trigger (`workflow_dispatch`).
2.  **Fetch**: Reach out to a public API to get a unique piece of data (Quote of the Day).
3.  **Update**: Append the new data to `data.txt`.
4.  **Commit**: Push the change using your GitHub identity to maintain your profile's green heatmap.

## 🚀 Setup & Customization

### 1. Fork this Repository
Click the **Fork** button at the top right to create your own copy.

### 2. Enable GitHub Actions
Navigate to the **Actions** tab in your fork and click **"I understand my workflows, go ahead and enable them"**.

### 3. Personalize your Identity
To make the commits count as yours, edit `.github/workflows/auto-commit.yml` and replace the placeholder email with your GitHub primary email:

```yaml
- name: Commit and Push
  run: |
    git config --global user.name "Your Name"
    git config --global user.email "your-email@example.com"
```

## 📈 Contribution Graph

By using this bot, you can ensure your GitHub profile reflects your daily commitment to your craft.

---

> [!TIP]
> **Want to change the frequency?** Edit the `cron` expression in `.github/workflows/auto-commit.yml`. For once-a-day runs, use `'0 0 * * *'`.

*Crafted by Mufeez Qadri & Antigravity.*
