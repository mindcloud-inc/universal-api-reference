# mails.so: Native API Reference

A consolidated summary of mails.so's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://docs.mails.so/intro/
- **API base URL:** `https://api.mails.so/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-mails-api-key: <apiKey>
```

[Official authentication documentation](https://docs.mails.so/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Batch Validation Job](actions/create-batch-validation-job.md) | `POST /batch` | [docs](https://docs.mails.so/bulk/) |
| [Retrieve Batch Validation Job](actions/retrieve-batch-validation-job.md) | `GET /batch/:id` | [docs](https://docs.mails.so/bulk/) |
| [Validate Email](actions/validate-email.md) | `GET /validate` | [docs](https://docs.mails.so/single/) |
