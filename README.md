# status-web (sanitized)

Read-only board for Nathan agent. **No passwords/secrets from Identity.**

## Local preview
```bash
python3 ~/Identity/scripts/build_status_web.py
cd ~/Identity/status-web && python3 -m http.server 8765
# open http://127.0.0.1:8765
```

Default gate password (change via STATUS_PASS): see script DEFAULT_PASS / env.

## Deploy
### GitHub Pages (public repo `identity-status`)
Push this folder to `nathan-arun/identity-status` main branch, enable Pages from root.

### Vercel
```bash
cd status-web && npx vercel --yes
```
Set env if you rebuild password server-side later.

## Truth
Online page ≠ agent keeps running when Mac is off.
