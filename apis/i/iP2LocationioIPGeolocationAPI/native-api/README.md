# IP2Location.io IP Geolocation: Native API Reference

A consolidated summary of IP2Location.io IP Geolocation's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://www.ip2location.io/documentation
- **API base URL:** `https://api.ip2location.io`

## Authentication

### API Key

Use an IP2Location.io API key. MindCloud sends it as the required query parameter named key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.ip2location.io/ip2location-documentation)

## API conventions

The total page count is read from `totalPages`. The current page number is read from `page`.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get IP Geolocation](actions/get-ip-geolocation.md) | `GET /` | [docs](https://www.ip2location.io/ip2location-documentation) |
| [List Hosted Domains by IP](actions/list-hosted-domains-by-ip.md) | `GET https://domains.ip2whois.com/domains` | [docs](https://www.ip2location.io/ip2whois-domains-documentation) |
| [Lookup Domain WHOIS](actions/lookup-domain-whois.md) | `GET https://api.ip2whois.com/v2` | [docs](https://www.ip2location.io/ip2whois-documentation) |
