# IP2WHOIS: Native API Reference

A consolidated summary of IP2WHOIS's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://www.ip2location.io/documentation
- **API base URL:** `https://api.ip2whois.com`

## Authentication

### API Key

Use your IP2WHOIS API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.ip2location.io/ip2whois-documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Hosted Domains by IP](actions/list-hosted-domains-by-ip.md) | `GET https://domains.ip2whois.com/domains` | [docs](https://www.ip2location.io/ip2whois-domains-documentation) |
| [Lookup Domain WHOIS](actions/lookup-domain-whois.md) | `GET /v2` | [docs](https://www.ip2location.io/ip2whois-documentation) |
