# Campaign Dashboard Event Listing Widget

An embeddable widget that displays upcoming volunteer opportunities from a [Campaign Dashboard](https://www.campaigndashboard.app) campaign. It shows each event with its title, date, time, location, and a sign-up link — and it refreshes automatically every time someone loads the page.

Originally built for the Burnaby Citizens Association, but easy to adapt for any Campaign Dashboard campaign. No coding experience required.

---

## Setting this up for your own campaign

You'll need a free [GitHub](https://github.com) account. GitHub is a website that can host simple web pages for free — that's all we're using it for here.

### Step 1: Create a GitHub account (if you don't have one)

1. Go to [github.com](https://github.com) and click **Sign up**
2. Follow the steps to create a free account

### Step 2: Fork this project

"Forking" makes a copy of this project under your own GitHub account, which you can then customize.

1. Make sure you're signed in to GitHub
2. Go to the top of this page and click the **Fork** button (top-right area)
3. On the next screen, you can leave everything as-is and click **Create fork**

You now have your own copy of the project.

### Step 3: Find your campaign slug

Your campaign slug is the short code in your Campaign Dashboard URL. For example, if your Campaign Dashboard address is:

```
https://www.campaigndashboard.app/xyz/campaign/
```

...then your slug is `xyz`.

Make a note of it — you'll need it in the next step.

### Step 4: Update the campaign slug in the code

1. In your forked repo, click on the file **`index.html`**
2. Click the **pencil icon** (Edit this file) near the top-right of the file view
3. Use your browser's find feature (**Ctrl+F** on Windows, **Cmd+F** on Mac) to search for:
   ```
   var CAMPAIGN = 'bca';
   ```
4. Replace `bca` with your own campaign slug (from Step 3), keeping the quote marks. For example:
   ```
   var CAMPAIGN = 'xyz';
   ```
5. Scroll down and click the green **Commit changes** button
6. In the dialog that appears, click **Commit changes** again to confirm

### Step 5: Enable GitHub Pages

This step publishes your widget as a live web page.

1. In your forked repo, click **Settings** (the tab along the top)
2. In the left sidebar, click **Pages**
3. Under **Source**, click the dropdown and select **Deploy from a branch**
4. Set the branch to **main** and the folder to **/ (root)**
5. Click **Save**

Within a minute or two, your widget will be live at:

```
https://YOUR_GITHUB_USERNAME.github.io/dashboard_events_listing/
```

(Replace `YOUR_GITHUB_USERNAME` with your actual GitHub username.)

You can visit that URL to confirm it's working before embedding it.

### Step 6: Embed the widget on your website

To add the listing to an existing webpage, paste the following code into your site wherever you want the listing to appear. Replace the URL with your own GitHub Pages address from Step 5.

```html
<iframe 
  src="https://YOUR_GITHUB_USERNAME.github.io/dashboard_events_listing/" 
  width="100%" 
  height="500" 
  frameborder="0"
  scrolling="auto">
</iframe>
```

If your website uses a page builder (like Squarespace, Wix, or WordPress), look for an option to add an "Embed" or "HTML" block, and paste the code there.

---

## How it works

When someone visits the page, it fetches the current list of public shifts directly from the Campaign Dashboard API and displays them. No API keys, passwords, or servers are involved — it's a single HTML file.
