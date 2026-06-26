# Campaign Dashboard Event Listing Widget

An embeddable widget that displays upcoming volunteer opportunities from a [Campaign Dashboard](https://www.campaigndashboard.app) campaign. Hosted on GitHub Pages, it fetches live shift data and shows each event with its title, date, time, location, and a sign-up link.

Originally built for the Burnaby Citizens Association — but easy to adapt for any Campaign Dashboard campaign.

## How it works

The page fetches live shift data from the Campaign Dashboard API on each load. No server, build step, or API key required — it's a single static HTML file.

## Using this for your own campaign

### 1. Fork or clone this repo

**Fork** (easiest): Click the **Fork** button at the top of this GitHub page. This creates a copy under your own GitHub account.

**Or clone** and push to a new repo:
```bash
git clone https://github.com/michaelroy-yvr/dashboard_events_listing.git
cd dashboard_events_listing
# Create a new repo on GitHub, then:
git remote set-url origin git@github.com:YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

### 2. Set your campaign slug

Open `index.html` and find this line near the top of the `<script>` block:

```js
var CAMPAIGN = 'bca';
```

Replace `bca` with your campaign's slug — the short code that appears in your Campaign Dashboard URL (e.g. `https://www.campaigndashboard.app/xyz/campaign/` → slug is `xyz`).

Save and commit the change:
```bash
git add index.html
git commit -m "Set campaign slug"
git push
```

### 3. Enable GitHub Pages

1. Go to your repo on GitHub
2. Click **Settings** → **Pages**
3. Under **Source**, select **Deploy from a branch**, choose `main`, folder `/ (root)`, and click **Save**

Your widget will be live at `https://YOUR_USERNAME.github.io/YOUR_REPO/` within a minute or two.

## Embedding

Add this iframe to any page where you want the listing to appear, substituting your own GitHub Pages URL:

```html
<iframe 
  src="https://YOUR_USERNAME.github.io/YOUR_REPO/" 
  width="100%" 
  height="500" 
  frameborder="0"
  scrolling="auto">
</iframe>
```

The listing refreshes every time a visitor loads the page, so it always reflects the current shifts in Campaign Dashboard.
