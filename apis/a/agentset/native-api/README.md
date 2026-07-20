# Agentset: Native API Reference

A consolidated summary of Agentset's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://docs.agentset.ai/api-reference/introduction
- **OpenAPI specification:** https://spec.speakeasy.com/agentset-ktc/api/agentset-api-with-code-samples
- **API base URL:** `https://api.agentset.ai`

## Authentication

### API Key

Use your Agentset API key. MindCloud sends it as Authorization: Bearer <api key>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.agentset.ai/api-reference/tokens)

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Batch Upload URLs](actions/create-batch-upload-urls.md) | `POST /v1/namespace/:namespaceId/uploads/batch` | [docs](https://docs.agentset.ai/api-reference/endpoint/uploads/batch) |
| [Create File Upload URL](actions/create-file-upload-url.md) | `POST /v1/namespace/:namespaceId/uploads` | [docs](https://docs.agentset.ai/api-reference/endpoint/uploads/single) |
| [Create Ingest Job](actions/create-ingest-job.md) | `POST /v1/namespace/:namespaceId/ingest-jobs` | [docs](https://docs.agentset.ai/api-reference/endpoint/ingest-jobs/create) |
| [Create Namespace](actions/create-namespace.md) | `POST /v1/namespace` | [docs](https://docs.agentset.ai/api-reference/endpoint/namespaces/create) |
| [Delete Document](actions/delete-document.md) | `DELETE /v1/namespace/:namespaceId/documents/:documentId` | [docs](https://docs.agentset.ai/api-reference/endpoint/documents/delete) |
| [Delete Hosting Configuration](actions/delete-hosting-configuration.md) | `DELETE /v1/namespace/:namespaceId/hosting` | [docs](https://docs.agentset.ai/api-reference/endpoint/hosting/delete) |
| [Delete Ingest Job](actions/delete-ingest-job.md) | `DELETE /v1/namespace/:namespaceId/ingest-jobs/:jobId` | [docs](https://docs.agentset.ai/api-reference/endpoint/ingest-jobs/delete) |
| [Delete Namespace](actions/delete-namespace.md) | `DELETE /v1/namespace/:namespaceId` | [docs](https://docs.agentset.ai/api-reference/endpoint/namespaces/delete) |
| [Enable Hosting](actions/enable-hosting.md) | `POST /v1/namespace/:namespaceId/hosting` | [docs](https://docs.agentset.ai/api-reference/endpoint/hosting/enable) |
| [Get Document Chunks Download URL](actions/get-document-chunks-download-url.md) | `POST /v1/namespace/:namespaceId/documents/:documentId/chunks-download-url` | [docs](https://docs.agentset.ai/api-reference/endpoint/documents/chunks-download-url) |
| [Get Document File Download URL](actions/get-document-file-download-url.md) | `POST /v1/namespace/:namespaceId/documents/:documentId/file-download-url` | [docs](https://docs.agentset.ai/api-reference/endpoint/documents/file-download-url) |
| [List Documents](actions/list-documents.md) | `GET /v1/namespace/:namespaceId/documents` | [docs](https://docs.agentset.ai/api-reference/endpoint/documents/list) |
| [List Ingest Jobs](actions/list-ingest-jobs.md) | `GET /v1/namespace/:namespaceId/ingest-jobs` | [docs](https://docs.agentset.ai/api-reference/endpoint/ingest-jobs/list) |
| [List Namespaces](actions/list-namespaces.md) | `GET /v1/namespace` | [docs](https://docs.agentset.ai/api-reference/endpoint/namespaces/list) |
| [Re-Ingest Job](actions/re-ingest-job.md) | `POST /v1/namespace/:namespaceId/ingest-jobs/:jobId/re-ingest` | [docs](https://docs.agentset.ai/api-reference/endpoint/ingest-jobs/re-ingest) |
| [Retrieve Document](actions/retrieve-document.md) | `GET /v1/namespace/:namespaceId/documents/:documentId` | [docs](https://docs.agentset.ai/api-reference/endpoint/documents/get) |
| [Retrieve Hosting Configuration](actions/retrieve-hosting-configuration.md) | `GET /v1/namespace/:namespaceId/hosting` | [docs](https://docs.agentset.ai/api-reference/endpoint/hosting/get) |
| [Retrieve Ingest Job](actions/retrieve-ingest-job.md) | `GET /v1/namespace/:namespaceId/ingest-jobs/:jobId` | [docs](https://docs.agentset.ai/api-reference/endpoint/ingest-jobs/get) |
| [Retrieve Namespace](actions/retrieve-namespace.md) | `GET /v1/namespace/:namespaceId` | [docs](https://docs.agentset.ai/api-reference/endpoint/namespaces/get) |
| [Search Namespace](actions/search-namespace.md) | `POST /v1/namespace/:namespaceId/search` | [docs](https://docs.agentset.ai/api-reference/endpoint/search) |
| [Update Hosting Configuration](actions/update-hosting-configuration.md) | `PATCH /v1/namespace/:namespaceId/hosting` | [docs](https://docs.agentset.ai/api-reference/endpoint/hosting/update) |
| [Update Namespace](actions/update-namespace.md) | `PATCH /v1/namespace/:namespaceId` | [docs](https://docs.agentset.ai/api-reference/endpoint/namespaces/update) |
| [Warm Namespace Cache](actions/warm-namespace-cache.md) | `POST /v1/namespace/:namespaceId/warm-up` | [docs](https://docs.agentset.ai/api-reference/endpoint/namespaces/warm-up) |
