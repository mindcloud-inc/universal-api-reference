# <img src="https://images.mindcloud.co/apps/icons/agentset_1776177058844.png" alt="Agentset logo" width="28" height="28"> Agentset: Universal API

Agentset is a RAG-as-a-service platform for namespaces, document ingestion, search, uploads, and hosting configuration management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/agentset/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://agentset.ai
- **Vendor API docs:** https://docs.agentset.ai/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Namespaces](actions/list-namespaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentset/latest/actions/list-namespaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes a document from Agentset. |
| [Get Document Chunks Download URL](actions/get-document-chunks-download-url.md) | GET | Retrieves a presigned download URL for document chunks from Agentset. |
| [Get Document File Download URL](actions/get-document-file-download-url.md) | GET | Retrieves a presigned download URL for a source file from Agentset. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from an Agentset namespace. |
| [Retrieve Document](actions/retrieve-document.md) | GET | Retrieves a document from Agentset by ID. |

### Hosting Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Delete Hosting Configuration](actions/delete-hosting-configuration.md) | DELETE | Deletes hosting configuration from Agentset. |
| [Enable Hosting](actions/enable-hosting.md) | POST | Enables hosting for an Agentset namespace. |
| [Retrieve Hosting Configuration](actions/retrieve-hosting-configuration.md) | GET | Retrieves hosting configuration from Agentset. |
| [Update Hosting Configuration](actions/update-hosting-configuration.md) | PUT | Updates hosting configuration in Agentset. |

### Ingest Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Ingest Job](actions/create-ingest-job.md) | POST | Creates an ingest job in an Agentset namespace. |
| [Delete Ingest Job](actions/delete-ingest-job.md) | DELETE | Deletes an ingest job from Agentset. |
| [List Ingest Jobs](actions/list-ingest-jobs.md) | GET | Retrieves ingest jobs from an Agentset namespace. |
| [Re-Ingest Job](actions/re-ingest-job.md) | POST | Starts re-ingestion for an Agentset ingest job. |
| [Retrieve Ingest Job](actions/retrieve-ingest-job.md) | GET | Retrieves an ingest job from Agentset by ID. |

### Namespace

| Action | Method | Description |
| --- | --- | --- |
| [Create Namespace](actions/create-namespace.md) | POST | Creates a new namespace in Agentset. |
| [Delete Namespace](actions/delete-namespace.md) | DELETE | Deletes a namespace from Agentset. |
| [List Namespaces](actions/list-namespaces.md) | GET | Retrieves all namespaces from Agentset. |
| [Retrieve Namespace](actions/retrieve-namespace.md) | GET | Retrieves a namespace from Agentset by ID. |
| [Update Namespace](actions/update-namespace.md) | PUT | Updates an existing namespace in Agentset. |
| [Warm Namespace Cache](actions/warm-namespace-cache.md) | POST | Starts a namespace cache warm-up in Agentset. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Namespace](actions/search-namespace.md) | GET | Searches an Agentset namespace by query. |

### Upload

| Action | Method | Description |
| --- | --- | --- |
| [Create Batch Upload URLs](actions/create-batch-upload-urls.md) | POST | Creates presigned batch file upload URLs in Agentset. |
| [Create File Upload URL](actions/create-file-upload-url.md) | POST | Creates a presigned file upload URL in Agentset. |

