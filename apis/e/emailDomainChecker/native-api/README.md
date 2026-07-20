# Email Domain Checker: Native API Reference

A consolidated summary of Email Domain Checker's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://mightora.io/tools/power-automate-connectors/email-domain-checker/
- **OpenAPI specification:** https://raw.githubusercontent.com/mightora/customConnectors/main/emailDomainChecker/swagger.json
- **API base URL:** `https://api.mightora.io/emailDomainChecker`

## Authentication

### API Key

Authenticate requests with the Mightora API key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-mightora-key: <apiKey>
```

[Official authentication documentation](https://learn.microsoft.com/en-gb/connectors/emaildomainchecker/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Domain](actions/check-domain.md) | `GET /checkDomain/` | [docs](https://learn.microsoft.com/en-gb/connectors/emaildomainchecker/#check-domain) |
