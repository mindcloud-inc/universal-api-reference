# Talend: Native API Reference

A consolidated summary of Talend's API configuration, with links to official documentation.

- **Official docs:** https://talend.qlik.dev/apis/
- **API base URL:** `https://api.us.cloud.talend.com`

## Authentication

### Personal Access Token

Use a Talend Cloud Personal Access Token. Talend requires the token in the Authorization header as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.qlik.com/talend/en-US/management-console-user-guide/Cloud/cloud-access-token)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.
