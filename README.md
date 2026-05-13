# Spark — A Tiny Daily Quote App

A single-page demo built end-to-end with AI for the BluestoneApps no-code
training session. The point of this app isn't the app — it's the workflow:

> A traditional developer can take an idea from "I have a thought" to
> "it's live on the internet" without writing a single line of code by hand.

## What it does

- Shows a random motivational quote on load.
- "New quote" button rotates to a fresh one with a small fade animation.
- Animated gradient background, glassmorphic card, mobile-friendly.

## Stack

- Pure static HTML/CSS/JS. No build step, no dependencies.
- A single `index.html` file — drop on any static host.

## Deployment

- **Source repo:** `smokyweb/spark-quote-app` on GitHub
- **Live URL:** `https://spark.bluesapps.com`
- **Hosting:** bluesapps.com (Nginx + static), pulled from GitHub.

## Training talking points

1. The developer describes the idea in plain English.
2. AI produces the full HTML/CSS/JS in one pass.
3. AI creates the GitHub repo, pushes the code, deploys to the server,
   configures Nginx, issues an SSL cert, and registers the app in the
   internal app directory.
4. The developer's job moves from "type code" to "review, steer, approve."

## Updating the app

1. Edit `index.html` (or let AI do it).
2. `git commit && git push`.
3. On the server: `cd /var/www/spark-quote-app && git pull && systemctl reload nginx` (only needed if Nginx config changed; for content-only changes, just `git pull`).
