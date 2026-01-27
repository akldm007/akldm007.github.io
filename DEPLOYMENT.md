# Deployment Guide

## GitHub Authentication Issue

GitHub no longer supports password authentication for Git operations. You have two options:

## Option 1: Using Personal Access Token (PAT) - Recommended

### Step 1: Create a Personal Access Token

1. Go to GitHub.com and log in
2. Click your profile picture → **Settings**
3. Scroll down and click **Developer settings** (left sidebar)
4. Click **Personal access tokens** → **Tokens (classic)**
5. Click **Generate new token** → **Generate new token (classic)**
6. Give it a name like "Blog Deployment"
7. Select expiration (recommend 90 days or No expiration)
8. Check these scopes:
   - ✅ `repo` (Full control of private repositories)
   - ✅ `workflow` (Update GitHub Action workflows)
9. Click **Generate token**
10. **IMPORTANT**: Copy the token NOW (you won't see it again!)

### Step 2: Use Token for Authentication

When pushing, use your token as the password:

```bash
cd akldm007.github.io
git add .
git commit -m "Modernize blog with 2025 design trends"
git push origin main
```

When prompted:
- **Username**: `akldm007`
- **Password**: Paste your Personal Access Token (not your GitHub password!)

### Step 3: Save Token (Optional but Recommended)

To avoid entering the token every time:

```bash
# Cache credentials for 1 hour
git config --global credential.helper cache

# Or cache for longer (e.g., 1 week = 604800 seconds)
git config --global credential.helper 'cache --timeout=604800'

# Or store permanently (less secure but convenient)
git config --global credential.helper store
```

## Option 2: Using SSH Keys (More Secure)

### Step 1: Generate SSH Key

```bash
# Generate a new SSH key
ssh-keygen -t ed25519 -C "sean.li02@sap.com"

# Press Enter to accept default location
# Enter a passphrase (optional but recommended)
```

### Step 2: Add SSH Key to GitHub

```bash
# Copy your public key
cat ~/.ssh/id_ed25519.pub
```

1. Go to GitHub.com → **Settings** → **SSH and GPG keys**
2. Click **New SSH key**
3. Paste your public key
4. Click **Add SSH key**

### Step 3: Test SSH Connection

```bash
ssh -T git@github.com
```

You should see: "Hi akldm007! You've successfully authenticated..."

### Step 4: Change Remote to SSH

```bash
cd akldm007.github.io
git remote set-url origin git@github.com:akldm007/akldm007.github.io.git
```

### Step 5: Push Changes

```bash
git push origin main
```

## Quick Deployment Commands

Once authentication is set up:

```bash
# Navigate to blog directory
cd akldm007.github.io

# Stage all changes
git add .

# Commit with message
git commit -m "Modernize blog with 2025 design trends"

# Push to GitHub
git push origin main
```

## Verify Deployment

After pushing:
1. Go to https://github.com/akldm007/akldm007.github.io
2. Click **Actions** tab to see build status
3. Once complete, visit: https://akldm007.github.io

## Troubleshooting

### Token Not Working
- Make sure you're using the token as password, not your GitHub password
- Verify the token has `repo` scope enabled
- Check if the token hasn't expired

### SSH Not Working
- Verify SSH key is added to GitHub
- Test connection: `ssh -T git@github.com`
- Make sure you changed remote URL to SSH format

### Build Failing on GitHub Pages
- Check the Actions tab for error messages
- Verify `_config.yml` syntax is correct
- Make sure all required plugins are listed

## Need Help?

If you continue to have issues:
1. Check GitHub's documentation: https://docs.github.com/en/authentication
2. Verify your repository settings on GitHub
3. Contact GitHub Support if needed

---

**Recommendation**: Use Personal Access Token for quick setup, or SSH keys for long-term secure access.
