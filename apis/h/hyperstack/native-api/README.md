# Hyperstack Certificates: Native API Reference

A consolidated summary of Hyperstack Certificates's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://thehyperstack.com/docs/api-guide/overview
- **API base URL:** `https://api.thehyperstack.com/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://thehyperstack.com/docs/api-guide/auth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |
| `content-type` | `application/json` |

Responses from this API use JSON.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | `POST /auth` | [docs](https://thehyperstack.com/docs/api-guide/auth) |
| [Create Credential Group](actions/create-credential-group.md) | `POST /groups/new` | [docs](https://thehyperstack.com/docs/api-guide/create-credential-group) |
| [Generate Credential Draft](actions/generate-credential-draft.md) | `POST /credentials/generate` | [docs](https://thehyperstack.com/docs/api-guide/generate-credential) |
| [Issue Credential](actions/issue-credential.md) | `POST /credentials/new` | [docs](https://thehyperstack.com/docs/api-guide/create-credential) |
| [List All Credentials](actions/list-all-credentials.md) | `POST /credentials/all` | [docs](https://thehyperstack.com/docs/api-guide/list-credentials) |
| [List All Groups](actions/list-all-groups.md) | `POST /groups/all` | [docs](https://thehyperstack.com/docs/api-guide/list-groups) |
| [Publish Credential](actions/publish-credential.md) | `POST /credential/:document_id/publish` | [docs](https://thehyperstack.com/docs/api-guide/publish-credential) |
| [Search Credentials](actions/search-credentials.md) | `POST /credentials/search` | [docs](https://thehyperstack.com/docs/api-guide/search-credentials) |
| [Search Groups](actions/search-groups.md) | `POST /groups/search` | [docs](https://thehyperstack.com/docs/api-guide/search-groups) |
| [Subscribe to Webhook](actions/subscribe-to-webhook.md) | `POST /webhook/subscribe` | [docs](https://thehyperstack.com/docs/api-guide/webhook-subscribe) |
| [Unsubscribe from Webhook](actions/unsubscribe-from-webhook.md) | `POST /webhook/unsubscribe` | [docs](https://thehyperstack.com/docs/api-guide/webhook-unsubscribe) |
| [Update Credential](actions/update-credential.md) | `POST /credential/:document_id/update` | [docs](https://thehyperstack.com/docs/api-guide/update-credential) |
| [Update Credential Group](actions/update-credential-group.md) | `POST /group/update/:group_key` | [docs](https://thehyperstack.com/docs/api-guide/update-credential-group) |
| [Update Recipient](actions/update-recipient.md) | `POST /recipients/update` | [docs](https://thehyperstack.com/docs/api-guide/update-recipient) |
| [View Credential](actions/view-credential.md) | `GET /credential/:document_id/view` | [docs](https://thehyperstack.com/docs/api-guide/view-credential) |
| [View Credential Group](actions/view-credential-group.md) | `GET /group/view/:group_key` | [docs](https://thehyperstack.com/docs/api-guide/view-credential-group) |
