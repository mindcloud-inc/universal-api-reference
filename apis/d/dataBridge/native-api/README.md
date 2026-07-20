# DataBridge: Native API Reference

A consolidated summary of DataBridge's API configuration and 71 documented operations, with links to official documentation.

- **Official docs:** https://www.morphik.ai/docs/api-reference/getting-started
- **OpenAPI specification:** https://api.morphik.ai/openapi.json
- **API base URL:** `https://api.morphik.ai`

## Authentication

### API Key

Use a Morphik API token. Morphik API requests authenticate with Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.morphik.ai/docs/api-reference/getting-started)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (71 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Document To Folder](actions/add-document-to-folder.md) | `POST /folders/:folder_id_or_name/documents/:document_id` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Batch Get Chunks](actions/batch-get-chunks.md) | `POST /batch/chunks` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Batch Get Documents](actions/batch-get-documents.md) | `POST /batch/documents` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Batch Ingest Files](actions/batch-ingest-files.md) | `POST /ingest/files` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Connector Oauth Callback](actions/connector-oauth-callback.md) | `GET /ee/connectors/:connector_type/oauth2callback` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Create Folder](actions/create-folder.md) | `POST /folders` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Delete Cloud App](actions/delete-cloud-app.md) | `DELETE /apps` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Delete Document](actions/delete-document.md) | `DELETE /documents/:document_id` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Delete Document V2](actions/delete-document-v2.md) | `DELETE /v2/documents/:document_id` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /folders/:folder_id_or_name` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Delete Model](actions/delete-model.md) | `DELETE /models/:model_id` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Disconnect Connector](actions/disconnect-connector.md) | `POST /ee/connectors/disconnect` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Download Document File](actions/download-document-file.md) | `GET /documents/:document_id/file` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Extract Document Pages](actions/extract-document-pages.md) | `POST /documents/pages` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Finalize Auth](actions/finalize-auth.md) | `POST /ee/connectors/finalize-auth` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Finalize Manual Auth](actions/finalize-manual-auth.md) | `POST /ee/connectors/:connector_type/auth/finalize` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Folder Details](actions/folder-details.md) | `POST /folders/details` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Generate Cloud Uri](actions/generate-cloud-uri.md) | `POST /cloud/generate_uri` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Get App Storage Usage](actions/get-app-storage-usage.md) | `GET /usage/app-storage` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Get Auth Status For Connector](actions/get-auth-status-for-connector.md) | `GET /ee/connectors/:connector_type/auth_status` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Get Available Models](actions/get-available-models.md) | `GET /models` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Get Available Models For Selection](actions/get-available-models-for-selection.md) | `GET /models/available` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Get Chat History](actions/get-chat-history.md) | `GET /chat/:chat_id` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Get Connector Status](actions/get-connector-status.md) | `POST /ee/connectors/status` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Get Document](actions/get-document.md) | `GET /documents/:document_id` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Get Document By Filename](actions/get-document-by-filename.md) | `GET /documents/filename/:filename` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Get Document Download URL](actions/get-document-download-url.md) | `GET /documents/:document_id/download_url` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Get Document Status](actions/get-document-status.md) | `GET /documents/:document_id/status` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Get Document Summary](actions/get-document-summary.md) | `GET /documents/:document_id/summary` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Get Folder](actions/get-folder.md) | `GET /folders/:folder_id_or_name` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Get Folder Summary](actions/get-folder-summary.md) | `GET /folders/:folder_id_or_name/summary` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Get Initiate Auth Url](actions/get-initiate-auth-url.md) | `GET /ee/connectors/:connector_type/auth/initiate_url` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Get Logs](actions/get-logs.md) | `GET /logs/` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Health Check](actions/health-check.md) | `GET /health` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Ingest Connector File](actions/ingest-connector-file.md) | `POST /ee/connectors/:connector_type/ingest` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Ingest Document V2](actions/ingest-document-v2.md) | `POST /v2/documents` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Ingest File](actions/ingest-file.md) | `POST /ingest/file` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Ingest Repository](actions/ingest-repository.md) | `POST /ee/connectors/:connector_type/ingest-repository` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Ingest Text](actions/ingest-text.md) | `POST /ingest/text` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Initiate Auth](actions/initiate-auth.md) | `POST /ee/connectors/initiate-auth` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [List Api Keys](actions/list-api-keys.md) | `GET /api-keys` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [List Chat Conversations](actions/list-chat-conversations.md) | `GET /chats` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [List Cloud Apps](actions/list-cloud-apps.md) | `GET /apps` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [List Connector Files](actions/list-connector-files.md) | `POST /ee/connectors/list-files` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [List Custom Models](actions/list-custom-models.md) | `GET /models/custom` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [List Docs](actions/list-docs.md) | `POST /documents` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [List Docs (Legacy Route)](actions/list-docs-legacy-route.md) | `POST /documents/list_docs` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [List Files For Connector](actions/list-files-for-connector.md) | `GET /ee/connectors/:connector_type/files` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [List Folder Summaries](actions/list-folder-summaries.md) | `GET /folders/summary` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [List Folders](actions/list-folders.md) | `GET /folders` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Move Folder](actions/move-folder.md) | `POST /folders/:folder_id_or_name/move` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Ping Health](actions/ping-health.md) | `GET /ping` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Query Completion](actions/query-completion.md) | `POST /query` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Query Document](actions/query-document.md) | `POST /ingest/document/query` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Remove Document From Folder](actions/remove-document-from-folder.md) | `DELETE /folders/:folder_id_or_name/documents/:document_id` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Rename Cloud App](actions/rename-cloud-app.md) | `PATCH /apps/rename` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Requeue Ingest Jobs](actions/requeue-ingest-jobs.md) | `POST /ingest/requeue` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Retrieve Chunks](actions/retrieve-chunks.md) | `POST /retrieve/chunks` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Retrieve Chunks Grouped](actions/retrieve-chunks-grouped.md) | `POST /retrieve/chunks/grouped` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Retrieve Chunks V2](actions/retrieve-chunks-v2.md) | `POST /v2/retrieve/chunks` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Retrieve Documents](actions/retrieve-documents.md) | `POST /retrieve/docs` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Rotate App Token](actions/rotate-app-token.md) | `POST /apps/rotate_token` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Save API Key](actions/save-api-key.md) | `POST /api-keys` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Save Model](actions/save-model.md) | `POST /models` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Search Documents By Name](actions/search-documents-by-name.md) | `POST /search/documents` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Update Chat Title](actions/update-chat-title.md) | `PATCH /chats/:chat_id/title` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Update Document File](actions/update-document-file.md) | `POST /documents/:document_id/update_file` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Update Document Metadata](actions/update-document-metadata.md) | `POST /documents/:document_id/update_metadata` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Update Document Text](actions/update-document-text.md) | `POST /documents/:document_id/update_text` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Upsert Document Summary](actions/upsert-document-summary.md) | `PUT /documents/:document_id/summary` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
| [Upsert Folder Summary](actions/upsert-folder-summary.md) | `PUT /folders/:folder_id_or_name/summary` | [docs](https://www.morphik.ai/docs/api-reference/getting-started) |
