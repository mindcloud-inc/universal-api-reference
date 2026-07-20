# DynaPictures: Native API Reference

A consolidated summary of DynaPictures's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://dynapictures.com/docs/
- **API base URL:** `https://api.dynapictures.com`

## Authentication

### API Key

Connect with a DynaPictures API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://dynapictures.com/docs/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `p` in the query string to choose the page; numbering starts at 1.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | `POST /workspaces` | [docs](https://dynapictures.com/docs/#create-workspace) |
| [Delete Asset](actions/delete-asset.md) | `DELETE /media/:workspaceId/assets/:id` | [docs](https://dynapictures.com/docs/#delete-asset) |
| [Delete Generated Image](actions/delete-generated-image.md) | `DELETE /images/:imagePath` | [docs](https://dynapictures.com/docs/#delete-generated-image) |
| [Delete Workspace](actions/delete-workspace.md) | `DELETE /workspaces/:id` | [docs](https://dynapictures.com/docs/#delete-workspace) |
| [Generate Image](actions/generate-image.md) | `POST /designs/:uid` | [docs](https://dynapictures.com/docs/#image-generation) |
| [Generate Multipage Images](actions/generate-multipage-images.md) | `POST /designs/:uid` | [docs](https://dynapictures.com/docs/#multipage-templates) |
| [Generate Multipage PDF](actions/generate-multipage-pdf.md) | `POST /batch` | [docs](https://dynapictures.com/docs/#multipage-pdf) |
| [Generate Template PDF](actions/generate-template-pdf.md) | `POST /designs/:uid` | [docs](https://dynapictures.com/docs/#pdf-generation) |
| [Get Asset](actions/get-asset.md) | `GET /media/:workspaceId/assets/:id` | [docs](https://dynapictures.com/docs/#load-asset) |
| [Get Template](actions/get-template.md) | `GET /templates/:uid` | [docs](https://dynapictures.com/docs/#get-template) |
| [List Assets](actions/list-assets.md) | `GET /media/:workspaceId/assets` | [docs](https://dynapictures.com/docs/#asset-list) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://dynapictures.com/docs/#list-templates) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://dynapictures.com/docs/#workspace-list) |
| [Subscribe Webhook](actions/subscribe-webhook.md) | `POST /hooks` | [docs](https://dynapictures.com/docs/#subscribe-webhook) |
| [Unsubscribe Webhook](actions/unsubscribe-webhook.md) | `DELETE /hooks` | [docs](https://dynapictures.com/docs/#unsubscribe-webhook) |
| [Update Asset](actions/update-asset.md) | `PUT /media/:workspaceId/assets/:id` | [docs](https://dynapictures.com/docs/#update-asset) |
| [Update Workspace](actions/update-workspace.md) | `PUT /workspaces/:id` | [docs](https://dynapictures.com/docs/#update-workspace) |
| [Upload Asset](actions/upload-asset.md) | `POST /media/:workspaceId/assets` | [docs](https://dynapictures.com/docs/#upload-an-image) |
