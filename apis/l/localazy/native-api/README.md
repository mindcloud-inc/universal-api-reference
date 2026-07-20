# Localazy: Native API Reference

A consolidated summary of Localazy's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://localazy.com/docs/api/introduction
- **API base URL:** `https://api.localazy.com`

## Authentication

### Project Token

Use a Localazy project token for REST API calls. Optionally add readKey and writeKey for CLI upload and download flows.

### Credentials

- **API Key:** `apiKey` · required
- **Read Key:** `readKey` · optional · Localazy CLI read key used for download flows.
- **Write Key:** `writeKey` · optional · Localazy CLI write key used for upload flows.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://localazy.com/docs/api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Glossary Term](actions/create-glossary-term.md) | `POST /projects/:projectId/glossary` | [docs](https://localazy.com/docs/api/glossary) |
| [Create Screenshot](actions/create-screenshot.md) | `POST /projects/:projectId/screenshots` | [docs](https://localazy.com/docs/api/screenshot-management) |
| [Delete Glossary Term](actions/delete-glossary-term.md) | `DELETE /projects/:projectId/glossary/:id` | [docs](https://localazy.com/docs/api/glossary) |
| [Delete Screenshot](actions/delete-screenshot.md) | `DELETE /projects/:projectId/screenshots/:screenshotId` | [docs](https://localazy.com/docs/api/screenshot-management) |
| [Delete Source Key](actions/delete-source-key.md) | `DELETE /projects/:projectId/keys/:keyId` | [docs](https://localazy.com/docs/api/source-keys) |
| [Download File](actions/download-file.md) | `GET /projects/:projectId/files/:fileId/download/:lang` | [docs](https://localazy.com/docs/api/files) |
| [Get Glossary Term](actions/get-glossary-term.md) | `GET /projects/:projectId/glossary/:id` | [docs](https://localazy.com/docs/api/glossary) |
| [Get Webhook Secret](actions/get-webhook-secret.md) | `GET /projects/:projectId/webhooks/secret` | [docs](https://localazy.com/docs/api/webhooks-api) |
| [Import Project Content](actions/import-project-content.md) | `POST /projects/:projectId/import` | [docs](https://localazy.com/docs/api/import) |
| [List CDN Metadata](actions/list-cdn-metadata.md) | `GET /projects/:projectId/cdn` | [docs](https://localazy.com/docs/api/cdn) |
| [List File Keys](actions/list-file-keys.md) | `GET /projects/:projectId/files/:fileId/keys/:lang` | [docs](https://localazy.com/docs/api/files) |
| [List Glossary Terms](actions/list-glossary-terms.md) | `GET /projects/:projectId/glossary` | [docs](https://localazy.com/docs/api/glossary) |
| [List Import Formats](actions/list-import-formats.md) | `GET /import/formats` | [docs](https://localazy.com/docs/api/import) |
| [List Project Files](actions/list-project-files.md) | `GET /projects/:projectId/files` | [docs](https://localazy.com/docs/api/files) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://localazy.com/docs/api/projects) |
| [List Screenshot Tags](actions/list-screenshot-tags.md) | `GET /projects/:projectId/screenshots/tags` | [docs](https://localazy.com/docs/api/screenshot-management) |
| [List Screenshots](actions/list-screenshots.md) | `GET /projects/:projectId/screenshots` | [docs](https://localazy.com/docs/api/screenshot-management) |
| [List Webhooks Configuration](actions/list-webhooks-configuration.md) | `GET /projects/:projectId/webhooks` | [docs](https://localazy.com/docs/api/webhooks-api) |
| [Replace Screenshot Image](actions/replace-screenshot-image.md) | `POST /projects/:projectId/screenshots/:screenshotId` | [docs](https://localazy.com/docs/api/screenshot-management) |
| [Translate With AI](actions/translate-with-ai.md) | `POST /projects/:projectId/ai` | [docs](https://localazy.com/docs/api/ai-translation-api) |
| [Update Glossary Term](actions/update-glossary-term.md) | `PUT /projects/:projectId/glossary/:id` | [docs](https://localazy.com/docs/api/glossary) |
| [Update Screenshot Metadata](actions/update-screenshot-metadata.md) | `PUT /projects/:projectId/screenshots/:screenshotId` | [docs](https://localazy.com/docs/api/screenshot-management) |
| [Update Source Key](actions/update-source-key.md) | `PUT /projects/:projectId/keys/:keyId` | [docs](https://localazy.com/docs/api/source-keys) |
| [Update Webhooks Configuration](actions/update-webhooks-configuration.md) | `POST /projects/:projectId/webhooks` | [docs](https://localazy.com/docs/api/webhooks-api) |
