# Minelead: Native API Reference

A consolidated summary of Minelead's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://api.minelead.io/
- **OpenAPI specification:** https://api.minelead.io/media/api_docs/api_docs.yml
- **API base URL:** `https://api.minelead.io/v1`

## Authentication

### API Key

Connect Minelead with your personal API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://minelead.io/docs/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Lead](actions/add-lead.md) | `POST /leads/` | [docs](https://api.minelead.io/) |
| [Create Recipient List](actions/create-recipient-list.md) | `POST /campaigns/recipients/` | [docs](https://api.minelead.io/) |
| [Delete Lead](actions/delete-lead.md) | `DELETE /leads/` | [docs](https://api.minelead.io/) |
| [Detect Disposable Email](actions/detect-disposable-email.md) | `GET /detect-disposable` | [docs](https://api.minelead.io/) |
| [Find Professional Email](actions/find-professional-email.md) | `GET /find` | [docs](https://api.minelead.io/) |
| [Generate Tags](actions/generate-tags.md) | `POST /tags/` | [docs](https://api.minelead.io/) |
| [Get Account](actions/get-account.md) | `POST /account/` | [docs](https://api.minelead.io/) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://api.minelead.io/) |
| [List History](actions/list-history.md) | `GET /history` | [docs](https://api.minelead.io/) |
| [List Leads](actions/list-leads.md) | `GET /leads` | [docs](https://api.minelead.io/) |
| [List Recipient Lists](actions/list-recipient-lists.md) | `GET /campaigns-recipients` | [docs](https://api.minelead.io/) |
| [Search Company Emails](actions/search-company-emails.md) | `GET /search` | [docs](https://api.minelead.io/) |
| [Update Lead](actions/update-lead.md) | `PUT /leads/` | [docs](https://api.minelead.io/) |
| [Update Recipient List](actions/update-recipient-list.md) | `PUT /campaigns/recipients/` | [docs](https://api.minelead.io/) |
| [Validate Email](actions/validate-email.md) | `GET /validate` | [docs](https://api.minelead.io/) |
