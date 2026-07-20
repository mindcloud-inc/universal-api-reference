# Cloudmersive Security: Native API Reference

A consolidated summary of Cloudmersive Security's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://api.cloudmersive.com/docs/security.asp
- **OpenAPI specification:** https://api.cloudmersive.com/swagger/api/security
- **API base URL:** `https://api.cloudmersive.com`

## Authentication

### Cloudmersive API Key

Authenticate requests with a Cloudmersive API key in the Apikey header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Apikey: <apiKey>
```

[Official authentication documentation](https://api.cloudmersive.com/docs/security.asp)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check IP Bot Status](actions/check-ip-bot-status.md) | `POST /security/threat-detection/network/ip/is-bot` | [docs](https://api.cloudmersive.com/docs/security.asp) |
| [Check IP Threat](actions/check-ip-threat.md) | `POST /security/threat-detection/network/ip/is-threat` | [docs](https://api.cloudmersive.com/docs/security.asp) |
| [Check Tor Exit Node](actions/check-tor-exit-node.md) | `POST /security/threat-detection/network/ip/is-tor-node` | [docs](https://api.cloudmersive.com/docs/security.asp) |
| [Detect and Normalize XSS](actions/detect-and-normalize-xss.md) | `POST /security/threat-detection/content/xss/detect/string` | [docs](https://api.cloudmersive.com/docs/security.asp) |
| [Detect JSON Insecure Deserialization](actions/detect-json-insecure-deserialization.md) | `POST /security/threat-detection/content/insecure-deserialization/json/detect/string` | [docs](https://api.cloudmersive.com/docs/security.asp) |
| [Detect SQL Injection](actions/detect-sql-injection.md) | `POST /security/threat-detection/content/sql-injection/detect/string` | [docs](https://api.cloudmersive.com/docs/security.asp) |
| [Detect SSRF URL Threat](actions/detect-ssrf-url-threat.md) | `POST /security/threat-detection/network/url/ssrf/detect` | [docs](https://api.cloudmersive.com/docs/security.asp) |
| [Detect Threats in Text](actions/detect-threats-in-text.md) | `POST /security/threat-detection/content/automatic/detect/string` | [docs](https://api.cloudmersive.com/docs/security.asp) |
| [Detect XXE in XML](actions/detect-xxe-in-xml.md) | `POST /security/threat-detection/content/xxe/detect/xml/string` | [docs](https://api.cloudmersive.com/docs/security.asp) |
