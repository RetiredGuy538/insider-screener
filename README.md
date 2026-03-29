# Insider Buy + Value Screener

A personal stock screening tool that identifies companies with:
- **Below-average P/E ratios** relative to their industry peers
- **Substantial insider buying** by corporate officers and directors

Powered by the [Financial Modeling Prep](https://financialmodelingprep.com) API.

---

## Deploying to GitHub Pages

### Step 1 — Create a new GitHub repository
1. Go to [github.com](https://github.com) and sign in as **RetiredGuy538**
2. Click the **+** icon → **New repository**
3. Name it something like `insider-screener`
4. Leave it **Public** (required for free GitHub Pages)
5. Click **Create repository**

### Step 2 — Add the file
1. Open **GitHub Desktop**
2. Clone the new repo to your Mac
3. Copy `index.html` into the cloned folder
4. In GitHub Desktop: write a commit message like `Initial deploy`
5. Click **Commit to main**, then **Push origin**

### Step 3 — Enable GitHub Pages
1. Go to your repo on github.com
2. Click **Settings** → **Pages** (left sidebar)
3. Under **Source**, select **Deploy from a branch**
4. Set branch to **main**, folder to **/ (root)**
5. Click **Save**
6. Wait ~60 seconds, then your site will be live at:
   `https://retiredguy538.github.io/insider-screener/`

---

## Changing the Password

Open `index.html` in any text editor and find this line near the top of the `<script>` section:

```javascript
const SCREENER_PASSWORD = 'lakelife';
```

Change `lakelife` to whatever password you want. Save the file, commit, and push.
The password is stored in the browser's session storage — users need to re-enter
it if they close the tab, but not on every page refresh within the same session.

---

## Sharing Access

Share this URL with your friends:
```
https://retiredguy538.github.io/insider-screener/
```

Tell them the password separately (text, email, etc.). That's all they need.
Works on iPhone and iPad — just open in Safari.

---

## Updating the Screener

Whenever you want to update the tool:
1. Replace `index.html` in your local repo folder with the new version
2. Open GitHub Desktop → commit → push
3. Changes go live within ~60 seconds

---

## Important Notes

- **The repo is public** — anyone who finds the URL can see the source code,
  including the API key and password. The password gate stops casual visitors
  but is not cryptographically secure. For a personal tool shared with a few
  trusted friends, this is fine.
- If you ever want to rotate the API key, update line `const API = '...'`
  in `index.html`, commit, and push.
- FMP Starter plan allows 300 API calls/minute. A full "All Sectors" run
  uses roughly 150–200 calls spread over 60–90 seconds — well within limits.
