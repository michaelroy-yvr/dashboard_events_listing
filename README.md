# BCA Volunteer Event Listing

An embeddable widget that displays upcoming volunteer opportunities for the Burnaby Citizens Association. Hosted on GitHub Pages and powered by the [Campaign Dashboard](https://www.campaigndashboard.app) API.

## How it works

The page fetches live shift data from the Campaign Dashboard API on each load and displays each event with its title, date, time, location, and a link to the sign-up page. No server or build step required — it's a single static HTML file.

## Embedding

Add this iframe to any page where you want the listing to appear:

```html
<iframe 
  src="https://michaelroy-yvr.github.io/dashboard_events_listing/" 
  width="100%" 
  height="500" 
  frameborder="0"
  scrolling="auto">
</iframe>
```

## Configuration

To use this with a different Campaign Dashboard campaign, edit the top of the `<script>` block in `index.html`:

```js
var CAMPAIGN = 'bca'; // change to your campaign slug
```
