# Remove.bg: Native API Reference

A consolidated summary of Remove.bg's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://www.remove.bg/api
- **OpenAPI specification:** https://www.remove.bg/api/swagger.yaml
- **API base URL:** `https://api.remove.bg/v1.0`

## Authentication

### API Key

Authenticate remove.bg requests with your API key in the X-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://www.remove.bg/api)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `500,502,503,504`. Wait 1 ms before the first retry. Stop after 5 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | `GET /account` | [docs](https://www.remove.bg/api#api-reference) |
| [Remove Background](actions/remove-background.md) | `POST /removebg` | [docs](https://www.remove.bg/api#api-reference) |
| [Submit Improvement](actions/submit-improvement.md) | `POST /improve` | [docs](https://www.remove.bg/api#api-reference) |
