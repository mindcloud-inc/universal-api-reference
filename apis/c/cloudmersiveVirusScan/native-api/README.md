# Cloudmersive Virus Scan: Native API Reference

A consolidated summary of Cloudmersive Virus Scan's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://api.cloudmersive.com/docs/virus.asp
- **OpenAPI specification:** https://api.cloudmersive.com/swagger/api/virus
- **API base URL:** `https://api.cloudmersive.com`

## Authentication

### Cloudmersive API Key

Cloudmersive API key authentication. The key is sent as the Apikey request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Apikey: <apiKey>
```

[Official authentication documentation](https://api.cloudmersive.com/docs/virus.asp)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Advanced Scan File for Viruses](actions/advanced-scan-file-for-viruses.md) | `POST /virus/scan/file/advanced` | [docs](https://api.cloudmersive.com/docs/virus.asp#operation--virus-scan-file-advanced-post) |
| [Scan File for Viruses](actions/scan-file-for-viruses.md) | `POST /virus/scan/file` | [docs](https://api.cloudmersive.com/docs/virus.asp#operation--virus-scan-file-post) |
| [Scan Website for Threats](actions/scan-website-for-threats.md) | `POST /virus/scan/website` | [docs](https://api.cloudmersive.com/docs/virus.asp#operation--virus-scan-website-post) |
