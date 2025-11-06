# LayoffToLiftoff Claude API Proxy Worker

## What This Does
Securely proxies requests to Claude API without exposing API keys to the frontend.

## Setup

1. **Install Wrangler (if not installed):**
```bash
   npm install -g wrangler
```

2. **Login to Cloudflare:**
```bash
   wrangler login
```

3. **Set API Key Secret:**
```bash
   wrangler secret put ANTHROPIC_API_KEY
   # Paste your Anthropic API key when prompted
```

4. **Deploy Worker:**
```bash
   cd workers
   wrangler deploy
```

5. **Get Worker URL:**
   After deployment, you'll get a URL like:
   `https://layofftoliftoff-claude-proxy.YOUR-SUBDOMAIN.workers.dev`

6. **Update Frontend:**
   Replace the API endpoint in demo-react.html:
```javascript
   // Change this:
   fetch("https://api.anthropic.com/v1/messages", ...)
   
   // To this:
   fetch("https://layofftoliftoff-claude-proxy.YOUR-SUBDOMAIN.workers.dev", ...)
```

## Usage

The worker accepts the same request format as Claude API:
```javascript
POST /
{
  "model": "claude-sonnet-4-20250514",
  "max_tokens": 2000,
  "messages": [
    { "role": "user", "content": "Your prompt here" }
  ]
}
```

## Security
- API keys stored securely in Cloudflare
- CORS enabled for your domain
- Request validation
- Error handling
