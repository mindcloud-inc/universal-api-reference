# Salesforge: Native API Reference

A consolidated summary of Salesforge's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://api.salesforge.ai/public/v2/docs
- **API base URL:** `https://api.salesforge.ai`

## Authentication

### API Key

Authenticate Salesforge API requests with an API key from Settings > API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://www.salesforge.ai/integrations/zapier)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 10). Use `offset` in the query string as the record offset.

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Contacts To Sequence](actions/assign-contacts-to-sequence.md) | `PUT /public/v2/workspaces/:workspaceID/sequences/:sequenceID/contacts` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Bulk Create Contacts](actions/bulk-create-contacts.md) | `POST /public/v2/workspaces/:workspaceID/contacts/bulk` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Bulk Create DNCs](actions/bulk-create-dncs.md) | `POST /public/v2/workspaces/:workspaceID/dnc/bulk` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Confirm Sequence Contact Validation Results](actions/confirm-sequence-contact-validation-results.md) | `POST /public/v2/workspaces/:workspaceID/sequences/:sequenceID/contacts/validation/confirm` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Create Contact](actions/create-contact.md) | `POST /public/v2/workspaces/:workspaceID/contacts` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Create Product](actions/create-product.md) | `POST /public/v2/workspaces/:workspaceID/products` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Create Sequence](actions/create-sequence.md) | `POST /public/v2/workspaces/:workspaceID/sequences` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Create Webhook](actions/create-webhook.md) | `POST /public/v2/workspaces/:workspaceID/integrations/webhooks` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Create Workspace](actions/create-workspace.md) | `POST /public/v2/workspaces` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Delete Sequence](actions/delete-sequence.md) | `DELETE /public/v2/workspaces/:workspaceID/sequences/:sequenceID` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Get Contact](actions/get-contact.md) | `GET /public/v2/workspaces/:workspaceID/contacts/:contactID` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Get Product](actions/get-product.md) | `GET /public/v2/workspaces/:workspaceID/products/:productID` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Get Sequence](actions/get-sequence.md) | `GET /public/v2/workspaces/:workspaceID/sequences/:sequenceID` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Get Sequence Analytics](actions/get-sequence-analytics.md) | `GET /public/v2/workspaces/:workspaceID/sequences/:sequenceID/analytics` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Get Sequence Contact Sending Data](actions/get-sequence-contact-sending-data.md) | `GET /public/v2/workspaces/:workspaceID/sending-data` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Get Sequence Contact Validation Results](actions/get-sequence-contact-validation-results.md) | `GET /public/v2/workspaces/:workspaceID/sequences/:sequenceID/contacts/validation/result` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Get Sequence Contacts Count](actions/get-sequence-contacts-count.md) | `GET /public/v2/workspaces/:workspaceID/sequences/:sequenceID/contacts/count` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Get Webhook](actions/get-webhook.md) | `GET /public/v2/workspaces/:workspaceID/integrations/webhooks/:webhookID` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Get Workspace](actions/get-workspace.md) | `GET /public/v2/workspaces/:workspaceID` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Get Workspace Sequence Metrics](actions/get-workspace-sequence-metrics.md) | `GET /public/v2/workspaces/:workspaceID/sequence-metrics` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Import Lead To Sequence](actions/import-lead-to-sequence.md) | `PUT /public/v2/workspaces/:workspaceID/sequences/:sequenceID/import-lead` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [List Contacts](actions/list-contacts.md) | `GET /public/v2/workspaces/:workspaceID/contacts` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [List Custom Variables](actions/list-custom-variables.md) | `GET /public/v2/workspaces/:workspaceID/custom-vars` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [List Mailboxes](actions/list-mailboxes.md) | `GET /public/v2/workspaces/:workspaceID/mailboxes` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [List Primebox Labels](actions/list-primebox-labels.md) | `GET /public/v2/workspaces/:workspaceID/primebox-labels` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [List Products](actions/list-products.md) | `GET /public/v2/workspaces/:workspaceID/products` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [List Webhooks](actions/list-webhooks.md) | `GET /public/v2/workspaces/:workspaceID/integrations/webhooks` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [List Workspace Sequences](actions/list-workspace-sequences.md) | `GET /public/v2/workspaces/:workspaceID/sequences` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [List Workspace Threads](actions/list-workspace-threads.md) | `GET /public/v2/workspaces/:workspaceID/threads` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [List Workspaces](actions/list-workspaces.md) | `GET /public/v2/workspaces` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Skip Sequence Contact Validation Results](actions/skip-sequence-contact-validation-results.md) | `POST /public/v2/workspaces/:workspaceID/sequences/:sequenceID/contacts/validation/skip` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Start Sequence Contact Validation](actions/start-sequence-contact-validation.md) | `POST /public/v2/workspaces/:workspaceID/sequences/:sequenceID/contacts/validation/start` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Update Sequence](actions/update-sequence.md) | `PUT /public/v2/workspaces/:workspaceID/sequences/:sequenceID` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Update Sequence Schedules](actions/update-sequence-schedules.md) | `PUT /public/v2/workspaces/:workspaceID/sequences/:sequenceID/schedules` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Update Sequence Status](actions/update-sequence-status.md) | `PUT /public/v2/workspaces/:workspaceID/sequences/:sequenceID/status` | [docs](https://api.salesforge.ai/public/v2/docs) |
| [Update Sequence Steps](actions/update-sequence-steps.md) | `PUT /public/v2/workspaces/:workspaceID/sequences/:sequenceID/steps` | [docs](https://api.salesforge.ai/public/v2/docs) |
