# HF Space Keep-Alive

[![Status](https://img.shields.io/badge/status-active-success.svg)](../../actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A GitHub Actions service that automatically pings your Hugging Face Spaces to prevent them from going dormant after 48 hours of inactivity.

## Quick Start

1. Fork this repository
2. Add your Space URL to `spaces.txt`:
   ```
   https://your-username-your-space.hf.space
   ```
3. Commit and push
4. Your Space will be pinged automatically every 24 hours

## How It Works

- Workflow runs daily at 00:00 UTC
- Sends HTTP GET request to each registered Space
- Prevents 48-hour inactivity timeout
- Completely free using GitHub Actions

## Features

- Automatic daily pings
- No cost (free GitHub Actions quota)
- Simple registration via pull request
- URL validation and security checks
- Full transparency with public logs

## URL Format

```
https://username-spacename.hf.space
```

Requirements:
- HTTPS only
- Valid `*.hf.space` domain
- One per line in `spaces.txt`

## Workflow Triggers

- **Schedule**: Daily at 00:00 UTC (`0 0 * * *`)
- **Push**: When `spaces.txt` is modified
- **Manual**: Via Actions tab

## Monitoring

Check workflow status in the [Actions tab](../../actions) to see:
- Ping success/failure for each Space
- Response times
- Execution history

## Limitations

- One ping every 24 hours (12-hour safety margin)
- Dependent on GitHub Actions availability
- Not affiliated with Hugging Face
  
## Support

Check existing issues or create a new one for problems or questions.

## License

MIT License
