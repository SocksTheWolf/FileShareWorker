# FileShareWorker

A simple filesharing endpoint that uses Cloudflare's R2, Workers and Turnstile to serve up large files.

## Setup

1. Create an R2 Bucket
2. Create a turnstile widget. Set your site private key as a secret called `CAPTCHA_PRIV_KEY` via Wrangler
3. Update the toml files with your various settings and endpoints
4. Deploy to Cloudflare

## Usage

### Uploading

You can upload your files directly via wrangler or via the web dashboard on the management portal for your bucket

### Downloading

Your files will be accessible via your website + FILES_PATH + file name. Anything that doesn't exist will serve up a failure page.
