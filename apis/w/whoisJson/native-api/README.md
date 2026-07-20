# WhoisJson: Native API Reference

A consolidated summary of WhoisJson's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://whoisjson.com/documentation
- **OpenAPI specification:** https://whoisjson.com/swagger.json
- **API base URL:** `https://whoisjson.com/api/v1`

## Authentication

### API Key

Use your WhoisJSON API key. The provider requires the Authorization header to be formatted as TOKEN=<YOUR_API_KEY>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://whoisjson.com/documentation)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Whois Data](actions/get-whois-data.md) | `GET /whois` | [docs](https://whoisjson.com/whois-api) |
