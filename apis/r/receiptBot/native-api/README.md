# Receipt Bot: Native API Reference

A consolidated summary of Receipt Bot's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/14388213/2sA3kYjLPj
- **API base URL:** `https://api.receipt-bot.com`

## Authentication

### API Key

Authenticate with the Receipt Bot Organization API Key.

### Credentials

- **API Key:** `apiKey` · required
- **Business ID:** `businessId` · required · Receipt Bot business identifier used on API requests.

Send these headers with each API request:

```http
APIKey: <apiKey>
```

[Official authentication documentation](https://www.receipt-bot.com/blog/knowledge-base/configuring-api-custom-accounting-software-integration/)

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
| [Get Statement Details](actions/get-statement-details.md) | `POST /StatementDetails` | [docs](https://documenter.getpostman.com/view/14388213/2sA3kYjLPj) |
| [Upload File](actions/upload-file.md) | `POST /FileUpload` | [docs](https://documenter.getpostman.com/view/14388213/2sA3kYjLPj) |
