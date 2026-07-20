# Twig Business: Native API Reference

A consolidated summary of Twig Business's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://help.twig.so/product/developer-api/overview
- **API base URL:** `https://app.twig.so/api`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.twig.so/product/developer-api/authentication)

## Endpoints (5 documented)

| Operation | Method & path |
| --- | --- |
| [Get Lambda Logs](actions/get-lambda-logs.md) | `GET lambda-logs` |
| [Get Process Logs](actions/get-process-logs.md) | `GET process-logs/{id}` |
| [List Data Sources](actions/list-data-sources.md) | `GET data-specs` |
| [List Subscriptions](actions/list-subscriptions.md) | `GET subscriptions` |
| [Search Data Sources](actions/search-data-sources.md) | `GET data-specs` |
