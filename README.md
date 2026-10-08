# dotwallet-site

Static site for **wallet.dotwallet.app**:

- `/.well-known/apple-app-site-association` — passkey `webcredentials` for `RZMA2C6H3N.com.dotwallet.app`
- `/privacy.html` — privacy policy for App Store Connect
- GitHub Pages + custom domain `wallet.dotwallet.app`

DNS (GoDaddy): `CNAME` name `wallet` → `pratyakshgupta48.github.io`.

Not affiliated with Polkadot’s DOT ticker.

## Content-Type caveat (GitHub Pages)

GitHub Pages serves the extensionless AASA as `Content-Type: application/octet-stream`
(verified). Apple’s docs prefer `application/json`. Many teams still succeed with
`webcredentials` on Pages; if Apple’s CDN rejects the file, move the same repo to
**Cloudflare Pages** (free) which honors the `_headers` file above.

## DNS (GoDaddy)

| Type | Name | Value | TTL |
|------|------|-------|-----|
| CNAME | `wallet` | `pratyakshgupta48.github.io` | Default |

Do **not** put a proxy/orange-cloud challenge in front of the AASA path if you later use Cloudflare DNS.
