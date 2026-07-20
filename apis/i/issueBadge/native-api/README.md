# IssueBadge: Native API Reference

A consolidated summary of IssueBadge's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://app.issuebadge.com/docs/api-documentation.html
- **OpenAPI specification:** https://app.issuebadge.com/docs/api-swagger.yaml
- **API base URL:** `https://app.issuebadge.com/api/v1`

## Authentication

### API Key

Connect IssueBadge with a personal access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.issuebadge.com/docs/api-documentation.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Badge](actions/create-badge.md) | `POST /badge/create` | [docs](https://app.issuebadge.com/docs/api-documentation.html) |
| [Issue Badge to Recipient](actions/issue-badge-to-recipient.md) | `POST /issue/create` | [docs](https://app.issuebadge.com/docs/api-documentation.html) |
| [List Badges](actions/list-badges.md) | `GET /badge/getall` | [docs](https://app.issuebadge.com/docs/api-documentation.html) |
