# SendX: Native API Reference

A consolidated summary of SendX's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.sendx.io/api-reference/introduction
- **OpenAPI specification:** https://docs.sendx.io/swagger.yaml
- **API base URL:** `https://api.sendx.io/api/v1/rest`

## Authentication

### Team API Key

Authenticate SendX requests with the Team API key sent in the X-Team-ApiKey header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Team-ApiKey: <apiKey>
```

[Official authentication documentation](https://docs.sendx.io/api-reference/introduction.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `offset` in the query string as the record offset.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | `POST /campaign` | [docs](https://docs.sendx.io/api-reference/campaign/create-campaign) |
| [Create Custom Field](actions/create-custom-field.md) | `POST /customfield` | [docs](https://docs.sendx.io/api-reference/custom-field/create-custom-field) |
| [Create Email Template](actions/create-email-template.md) | `POST /template/email` | [docs](https://docs.sendx.io/api-reference/template/create-email-template) |
| [Create List](actions/create-list.md) | `POST /list` | [docs](https://docs.sendx.io/api-reference/list/create-list) |
| [Create Tag](actions/create-tag.md) | `POST /tag` | [docs](https://docs.sendx.io/api-reference/tag/create-tag) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaign/:identifier` | [docs](https://docs.sendx.io/api-reference/campaign/get-campaign-by-id) |
| [Get Campaign Report](actions/get-campaign-report.md) | `GET /report/campaign/:identifier` | [docs](https://docs.sendx.io/api-reference/report/get-campaign-report) |
| [Get Contact](actions/get-contact.md) | `GET /contact/:identifier` | [docs](https://docs.sendx.io/api-reference/contact/get-contact-by-id) |
| [Get Custom Field](actions/get-custom-field.md) | `GET /customfield/:identifier` | [docs](https://docs.sendx.io/api-reference/custom-field/get-custom-field-by-id) |
| [Get List](actions/get-list.md) | `GET /list/:identifier` | [docs](https://docs.sendx.io/api-reference/list/get-list-by-id) |
| [Get Tag](actions/get-tag.md) | `GET /tag/:identifier` | [docs](https://docs.sendx.io/api-reference/tag/get-tag-by-id) |
| [Get Template](actions/get-template.md) | `GET /template/email/:identifier` | [docs](https://docs.sendx.io/api-reference/template/get-template-by-id) |
| [Identify Bulk Contacts](actions/identify-bulk-contacts.md) | `POST /contact/identify/bulk` | [docs](https://docs.sendx.io/api-reference/getting-started/identify-contact-bulk) |
| [Identify Contact](actions/identify-contact.md) | `POST /contact/identify` | [docs](https://docs.sendx.io/api-reference/getting-started/identify-contact) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaign` | [docs](https://docs.sendx.io/api-reference/campaign/get-all-campaigns) |
| [List Contacts](actions/list-contacts.md) | `GET /contact` | [docs](https://docs.sendx.io/api-reference/contact/get-all-contacts) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /customfield` | [docs](https://docs.sendx.io/api-reference/custom-field/get-all-custom-fields) |
| [List Lists](actions/list-lists.md) | `GET /list` | [docs](https://docs.sendx.io/api-reference/list/get-all-lists) |
| [List Tags](actions/list-tags.md) | `GET /tag` | [docs](https://docs.sendx.io/api-reference/tag/get-all-tags) |
| [List Templates](actions/list-templates.md) | `GET /template/email` | [docs](https://docs.sendx.io/api-reference/template/get-all-templates) |
| [Update Contact](actions/update-contact.md) | `PUT /contact/:identifier` | [docs](https://docs.sendx.io/api-reference/contact/update-contact) |
| [Update Custom Field](actions/update-custom-field.md) | `PUT /customfield/:identifier` | [docs](https://docs.sendx.io/api-reference/custom-field/update-custom-field) |
| [Update List](actions/update-list.md) | `PUT /list/:identifier` | [docs](https://docs.sendx.io/api-reference/list/update-list) |
| [Update Tag](actions/update-tag.md) | `PUT /tag/:identifier` | [docs](https://docs.sendx.io/api-reference/tag/update-tag) |
