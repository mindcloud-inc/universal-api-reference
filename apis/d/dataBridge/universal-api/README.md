# <img src="https://images.mindcloud.co/apps/icons/morphik-icon_1776455846372.png" alt="DataBridge logo" width="28" height="28"> DataBridge: Universal API

Morphik is a document intelligence and retrieval platform for ingesting files and text, managing documents and folders, querying knowledge bases, managing chats, models, API keys, and cloud apps, and using enterprise connectors.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dataBridge/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 71
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.morphik.ai/
- **Vendor API docs:** https://www.morphik.ai/docs/api-reference/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Available Models](actions/get-available-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/get-available-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (71)

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [List Api Keys](actions/list-api-keys.md) | GET | Retrieves API keys from DataBridge. |
| [Save API Key](actions/save-api-key.md) | POST | Saves a provider API key in DataBridge. |

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Delete Cloud App](actions/delete-cloud-app.md) | DELETE | Deletes a cloud app and its resources from DataBridge. |
| [Generate Cloud Uri](actions/generate-cloud-uri.md) | POST | Generates an authenticated cloud app URI in DataBridge. |
| [List Cloud Apps](actions/list-cloud-apps.md) | GET | Retrieves cloud apps from DataBridge. |
| [Rename Cloud App](actions/rename-cloud-app.md) | PUT | Updates a cloud app name in DataBridge. |
| [Rotate App Token](actions/rotate-app-token.md) | POST | Rotates a cloud app token in DataBridge. |

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [Get Logs](actions/get-logs.md) | GET | Retrieves audit logs from DataBridge. |

### Connectors

| Action | Method | Description |
| --- | --- | --- |
| [Connector Oauth Callback](actions/connector-oauth-callback.md) | GET | Handles a connector OAuth callback in DataBridge. |
| [Disconnect Connector](actions/disconnect-connector.md) | PUT | Disconnects a connector and removes its credentials in DataBridge. |
| [Finalize Auth](actions/finalize-auth.md) | PUT | Finalizes authentication for a connector in DataBridge. |
| [Finalize Manual Auth](actions/finalize-manual-auth.md) | PUT | Finalizes connector authentication manually in DataBridge. |
| [Get Auth Status For Connector](actions/get-auth-status-for-connector.md) | GET | Retrieves connector auth status from DataBridge. |
| [Get Connector Status](actions/get-connector-status.md) | GET | Retrieves a connector's authentication status in DataBridge. |
| [Get Initiate Auth Url](actions/get-initiate-auth-url.md) | GET | Retrieves a connector auth URL from DataBridge. |
| [Ingest Connector File](actions/ingest-connector-file.md) | POST | Ingests a single file from a connector in DataBridge. |
| [Ingest Repository](actions/ingest-repository.md) | POST | Ingests an entire GitHub repository into DataBridge. |
| [Initiate Auth](actions/initiate-auth.md) | POST | Initiates the OAuth flow for a connector in DataBridge. |
| [List Connector Files](actions/list-connector-files.md) | GET | Retrieves files from a connector in DataBridge. |
| [List Files For Connector](actions/list-files-for-connector.md) | GET | Retrieves files and folders for a connector in DataBridge. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Get Chat History](actions/get-chat-history.md) | GET | Retrieves chat history from DataBridge. |
| [List Chat Conversations](actions/list-chat-conversations.md) | GET | Retrieves chat conversations from DataBridge. |
| [Update Chat Title](actions/update-chat-title.md) | PUT | Updates a chat title in DataBridge. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Batch Get Chunks](actions/batch-get-chunks.md) | GET | Retrieves document chunks from DataBridge in batches. |
| [Batch Get Documents](actions/batch-get-documents.md) | GET | Retrieves documents from DataBridge in batches. |
| [Batch Ingest Files](actions/batch-ingest-files.md) | POST | Creates documents in DataBridge from multiple files. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes a document from DataBridge. |
| [Delete Document V2](actions/delete-document-v2.md) | DELETE |  |
| [Download Document File](actions/download-document-file.md) | GET | Downloads a document file from DataBridge. |
| [Extract Document Pages](actions/extract-document-pages.md) | POST | Extracts pages from a document in DataBridge. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from DataBridge. |
| [Get Document By Filename](actions/get-document-by-filename.md) | GET | Retrieves a document from DataBridge by filename. |
| [Get Document Download URL](actions/get-document-download-url.md) | GET | Retrieves a document download URL from DataBridge. |
| [Get Document Status](actions/get-document-status.md) | GET | Retrieves a document's status from DataBridge. |
| [Get Document Summary](actions/get-document-summary.md) | GET | Retrieves a document summary from DataBridge. |
| [Ingest Document V2](actions/ingest-document-v2.md) | POST |  |
| [Ingest File](actions/ingest-file.md) | POST | Creates a document in DataBridge from a file. |
| [Ingest Text](actions/ingest-text.md) | POST | Creates a document in DataBridge from text. |
| [List Docs](actions/list-docs.md) | GET | Retrieves documents from the DataBridge workspace. |
| [List Docs (Legacy Route)](actions/list-docs-legacy-route.md) | GET | Retrieves documents from DataBridge using the legacy route. |
| [Requeue Ingest Jobs](actions/requeue-ingest-jobs.md) | PUT | Requeues document ingest jobs in DataBridge. |
| [Retrieve Chunks](actions/retrieve-chunks.md) | GET | Retrieves document chunks from DataBridge. |
| [Retrieve Chunks Grouped](actions/retrieve-chunks-grouped.md) | GET | Retrieves grouped document chunks from DataBridge. |
| [Retrieve Chunks V2](actions/retrieve-chunks-v2.md) | GET |  |
| [Retrieve Documents](actions/retrieve-documents.md) | GET | Retrieves matching documents from DataBridge. |
| [Search Documents By Name](actions/search-documents-by-name.md) | GET | Finds documents in DataBridge by filename. |
| [Update Document File](actions/update-document-file.md) | PUT | Updates a document file in DataBridge. |
| [Update Document Metadata](actions/update-document-metadata.md) | PUT | Updates document metadata in DataBridge. |
| [Update Document Text](actions/update-document-text.md) | PUT | Updates a document's text in DataBridge. |
| [Upsert Document Summary](actions/upsert-document-summary.md) | PUT | Creates or updates a document summary in DataBridge. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Add Document To Folder](actions/add-document-to-folder.md) | POST | Adds a document to a folder in DataBridge. |
| [Create Folder](actions/create-folder.md) | POST | Creates a folder in DataBridge. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes a folder from DataBridge. |
| [Folder Details](actions/folder-details.md) | POST | Retrieves folder details from DataBridge. |
| [Get Folder](actions/get-folder.md) | GET | Retrieves a folder from DataBridge. |
| [Get Folder Summary](actions/get-folder-summary.md) | GET | Retrieves a folder summary from DataBridge. |
| [List Folder Summaries](actions/list-folder-summaries.md) | GET | Retrieves folder summaries from DataBridge. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from the DataBridge workspace. |
| [Move Folder](actions/move-folder.md) | PUT |  |
| [Remove Document From Folder](actions/remove-document-from-folder.md) | DELETE | Removes a document from a folder in DataBridge. |
| [Upsert Folder Summary](actions/upsert-folder-summary.md) | PUT | Creates or updates a folder summary in DataBridge. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get App Storage Usage](actions/get-app-storage-usage.md) | GET | Retrieves app storage usage from DataBridge. |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Delete Model](actions/delete-model.md) | DELETE | Deletes a model from DataBridge. |
| [Get Available Models](actions/get-available-models.md) | GET | Retrieves available models from DataBridge. |
| [Get Available Models For Selection](actions/get-available-models-for-selection.md) | GET | Retrieves available models for selection in DataBridge. |
| [List Custom Models](actions/list-custom-models.md) | GET | Retrieves custom models from DataBridge. |
| [Save Model](actions/save-model.md) | POST | Saves a custom model configuration in DataBridge. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Query Completion](actions/query-completion.md) | GET | Generates a completion in DataBridge using relevant chunks. |
| [Query Document](actions/query-document.md) | GET | Runs a one-off document analysis in DataBridge. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | GET | Checks overall DataBridge service health. |
| [Ping Health](actions/ping-health.md) | GET | Checks the DataBridge ping endpoint. |

