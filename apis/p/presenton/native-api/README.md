# Presenton: Native API Reference

A consolidated summary of Presenton's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://docs.presenton.ai/api-reference
- **API base URL:** `https://api.presenton.ai`

## Authentication

### API Key

Authenticate to Presenton with a personal API key using the Authorization bearer header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.presenton.ai/using-presenton-api)

## Pagination

Use `page_size` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Presentation From JSON](actions/create-presentation-from-json.md) | `POST /api/v1/ppt/presentation/create/from-json` | [docs](https://docs.presenton.ai/api-reference/presentation/create-presentation-from-json-sync-v1) |
| [Create Presentation From JSON Async](actions/create-presentation-from-json-async.md) | `POST /api/v1/ppt/presentation/create/from-json/async` | [docs](https://docs.presenton.ai/api-reference/presentation/create-presentation-from-json-async-v1) |
| [Create Presentation From JSON Async V3](actions/create-presentation-from-json-async-v3.md) | `POST /api/v3/presentation/from-json/async` | [docs](https://docs.presenton.ai/api-reference/v3-presentation/create-presentation-from-json-async-v3) |
| [Create Presentation From JSON V3](actions/create-presentation-from-json-v3.md) | `POST /api/v3/presentation/from-json` | [docs](https://docs.presenton.ai/api-reference/v3-presentation/create-presentation-from-json-sync-v3) |
| [Delete Presentation](actions/delete-presentation.md) | `DELETE /api/v1/ppt/presentation/:id` | [docs](https://docs.presenton.ai/api-reference/presentation/delete-presentation-by-id) |
| [Derive Presentation](actions/derive-presentation.md) | `POST /api/v1/ppt/presentation/derive` | [docs](https://docs.presenton.ai/api-reference/presentation/derive-presentation-from-existing-one) |
| [Edit Presentation](actions/edit-presentation.md) | `POST /api/v1/ppt/presentation/edit` | [docs](https://docs.presenton.ai/api-reference/presentation/edit-presentation-with-new-content) |
| [Export Presentation](actions/export-presentation.md) | `POST /api/v1/ppt/presentation/export` | [docs](https://docs.presenton.ai/api-reference/presentation/export-presentation-as-pptx-or-pdf-v1) |
| [Export Presentation V3](actions/export-presentation-v3.md) | `POST /api/v3/presentation/export` | [docs](https://docs.presenton.ai/api-reference/v3-presentation/export-presentation-as-pptx-or-pdf-v3) |
| [Generate Presentation](actions/generate-presentation.md) | `POST /api/v1/ppt/presentation/generate` | [docs](https://docs.presenton.ai/api-reference/presentation/generate-presentation-sync-v1) |
| [Generate Presentation Async](actions/generate-presentation-async.md) | `POST /api/v1/ppt/presentation/generate/async` | [docs](https://docs.presenton.ai/api-reference/presentation/generate-presentation-async-v1) |
| [Generate Presentation Async V3](actions/generate-presentation-async-v3.md) | `POST /api/v3/presentation/generate/async` | [docs](https://docs.presenton.ai/api-reference/v3-presentation/generate-presentation-async-v3) |
| [Generate Presentation Outlines V3](actions/generate-presentation-outlines-v3.md) | `POST /api/v3/presentation/outlines/generate` | [docs](https://docs.presenton.ai/api-reference/v3-presentation/generate-outlines-sync-v3) |
| [Generate Presentation V3](actions/generate-presentation-v3.md) | `POST /api/v3/presentation/generate` | [docs](https://docs.presenton.ai/api-reference/v3-presentation/generate-presentation-sync-v3) |
| [Get Async Presentation Generation Status](actions/get-async-presentation-generation-status.md) | `GET /api/v1/ppt/presentation/status/:id` | [docs](https://docs.presenton.ai/api-reference/presentation/check-async-presentation-generation-status) |
| [Get Async Task Status V3](actions/get-async-task-status-v3.md) | `GET /api/v3/async-task/status/:id` | [docs](https://docs.presenton.ai/api-reference/v3-async-task/get-async-task-status) |
| [Get Credit Info](actions/get-credit-info.md) | `GET /api/v1/credit/info` | [docs](https://docs.presenton.ai/api-reference) |
| [Get Presentation](actions/get-presentation.md) | `GET /api/v1/ppt/presentation/:id` | [docs](https://docs.presenton.ai/api-reference/presentation/get-presentation-and-slides-by-id) |
| [Get Presentation Editor View](actions/get-presentation-editor-view.md) | `GET /api/v1/ppt/presentation/:id/ui` | [docs](https://docs.presenton.ai/api-reference) |
| [Get Standard Template](actions/get-standard-template.md) | `GET /api/v3/standard-template/:id` | [docs](https://docs.presenton.ai/api-reference/v3-standard-template/get-standard-template-by-id) |
| [Get Standard Template Example](actions/get-standard-template-example.md) | `GET /api/v3/standard-template/:id/example` | [docs](https://docs.presenton.ai/api-reference/v3-standard-template/get-standard-template-example) |
| [Get Template](actions/get-template.md) | `GET /api/v1/ppt/template/:id` | [docs](https://docs.presenton.ai/api-reference/template/get-template-by-id) |
| [Get Template Example](actions/get-template-example.md) | `GET /api/v1/ppt/template/:id/example` | [docs](https://docs.presenton.ai/api-reference/template/get-template-example) |
| [List Presentations](actions/list-presentations.md) | `GET /api/v1/ppt/presentation/all` | [docs](https://docs.presenton.ai/api-reference/presentation/get-all-user-presentations) |
| [List Presentations V3](actions/list-presentations-v3.md) | `GET /api/v3/presentation/all` | [docs](https://docs.presenton.ai/api-reference/v3-presentation/get-all-user-presentations-for-ui) |
| [List Presentations V3 Editor View](actions/list-presentations-v3-editor-view.md) | `GET /api/v3/presentation/all/ui` | [docs](https://docs.presenton.ai/api-reference) |
| [List Smart Designs](actions/list-smart-designs.md) | `GET /api/v3/smart-design/all` | [docs](https://docs.presenton.ai/api-reference/v3-smart-design/get-all-smart-designs) |
| [List Standard Templates](actions/list-standard-templates.md) | `GET /api/v3/standard-template/all` | [docs](https://docs.presenton.ai/api-reference/v3-standard-template/get-all-standard-templates) |
| [List Templates](actions/list-templates.md) | `GET /api/v1/ppt/template/all` | [docs](https://docs.presenton.ai/api-reference/template/get-all-templates) |
| [List Uploaded Images](actions/list-uploaded-images.md) | `GET /api/v1/ppt/images/uploaded` | [docs](https://docs.presenton.ai/api-reference/images/get-uploaded-images-v1) |
| [List Uploaded Images V3](actions/list-uploaded-images-v3.md) | `GET /api/v3/images/uploaded` | [docs](https://docs.presenton.ai/api-reference/v3-images/get-uploaded-images-v3) |
| [List Webhook Subscriptions V3](actions/list-webhook-subscriptions-v3.md) | `GET /api/v3/webhook/all` | [docs](https://docs.presenton.ai/api-reference/v3-webhook/get-all-webhook-subscriptions-v3) |
| [Subscribe to Webhook](actions/subscribe-to-webhook.md) | `POST /api/v1/webhook/subscribe` | [docs](https://docs.presenton.ai/api-reference/webhook/subscribe-to-webhook-v1) |
| [Subscribe to Webhook V3](actions/subscribe-to-webhook-v3.md) | `POST /api/v3/webhook/subscribe` | [docs](https://docs.presenton.ai/api-reference/v3-webhook/subscribe-to-webhook-v3) |
| [Unsubscribe All Webhook Subscriptions V3](actions/unsubscribe-all-webhook-subscriptions-v3.md) | `DELETE /api/v3/webhook/unsubscribe/all` | [docs](https://docs.presenton.ai/api-reference/v3-webhook/unsubscribe-all-webhook-subscriptions-v3) |
| [Unsubscribe from Webhook](actions/unsubscribe-from-webhook.md) | `DELETE /api/v1/webhook/unsubscribe` | [docs](https://docs.presenton.ai/api-reference/webhook/unsubscribe-to-webhook-v1) |
| [Unsubscribe from Webhook V3](actions/unsubscribe-from-webhook-v3.md) | `DELETE /api/v3/webhook/unsubscribe` | [docs](https://docs.presenton.ai/api-reference/v3-webhook/unsubscribe-to-webhook-v3) |
