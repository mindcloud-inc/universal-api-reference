# Papersign: Native API Reference

A consolidated summary of Papersign's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://paperform.readme.io/reference/getting-started-1
- **API base URL:** `https://api.paperform.co/v1`

## Authentication

### API Key

Bearer API key authentication for the Papersign API

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://paperform.readme.io/reference/getting-started-1)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Papersign Document](actions/cancel-papersign-document.md) | `PUT /papersign/documents/:id/cancel` | [docs](https://paperform.readme.io/reference/papersigncanceldocument) |
| [Copy Papersign Document](actions/copy-papersign-document.md) | `POST /papersign/documents/:id/copy` | [docs](https://paperform.readme.io/reference/papersigncopydocument) |
| [Create Papersign Folder](actions/create-papersign-folder.md) | `POST /papersign/folders` | [docs](https://paperform.readme.io/reference/postpapersignfolders) |
| [Create Papersign Folder Webhook](actions/create-papersign-folder-webhook.md) | `POST /papersign/folders/:id/webhooks` | [docs](https://paperform.readme.io/reference/postpapersignfolderwebhooks) |
| [Delete Papersign Folder Webhook](actions/delete-papersign-folder-webhook.md) | `DELETE /papersign/webhooks/:id` | [docs](https://paperform.readme.io/reference/deletepapersignfolderwebhooks) |
| [Get Papersign Document](actions/get-papersign-document.md) | `GET /papersign/documents/:id` | [docs](https://paperform.readme.io/reference/getpapersigndocument) |
| [List Papersign Documents](actions/list-papersign-documents.md) | `GET /papersign/documents` | [docs](https://paperform.readme.io/reference/listpapersigndocuments) |
| [List Papersign Folder Webhooks](actions/list-papersign-folder-webhooks.md) | `GET /papersign/folders/:id/webhooks` | [docs](https://paperform.readme.io/reference/getpapersignfolderwebhooks) |
| [List Papersign Folders](actions/list-papersign-folders.md) | `GET /papersign/folders` | [docs](https://paperform.readme.io/reference/listpapersignfolders) |
| [List Papersign Spaces](actions/list-papersign-spaces.md) | `GET /papersign/spaces` | [docs](https://paperform.readme.io/reference/listpapersignspaces) |
| [Move Papersign Document](actions/move-papersign-document.md) | `POST /papersign/documents/:id/move` | [docs](https://paperform.readme.io/reference/papersignmovedocument) |
| [Send Papersign Document](actions/send-papersign-document.md) | `POST /papersign/documents/:id/send` | [docs](https://paperform.readme.io/reference/papersignsenddocument) |
| [Update Papersign Folder Webhook](actions/update-papersign-folder-webhook.md) | `PUT /papersign/webhooks/:id` | [docs](https://paperform.readme.io/reference/putpapersignfolderwebhooks) |
