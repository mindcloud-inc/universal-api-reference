# Autype: Native API Reference

A consolidated summary of Autype's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.autype.com/api-reference/introduction
- **OpenAPI specification:** https://docs.autype.com/api-reference/openapi.json
- **API base URL:** `https://api.autype.com/api/v1/dev`

## Authentication

### Autype API Key

Connect Autype with an API key from Settings > API Keys. The Developer API accepts only keys that start with ak_.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.autype.com/api-reference/authentication)

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bulk Render Job From File](actions/create-bulk-render-job-from-file.md) | `POST /bulk-render/file` | [docs](https://docs.autype.com/api-reference/developer-api/create-bulk-render-job-from-file) |
| [Create Bulk Render Job From JSON](actions/create-bulk-render-job-from-json.md) | `POST /bulk-render` | [docs](https://docs.autype.com/api-reference/developer-api/create-bulk-render-job-from-json) |
| [Create Document](actions/create-document.md) | `POST /documents` | [docs](https://docs.autype.com/api-reference/developer-api/create-document) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://docs.autype.com/api-reference/developer-api/create-project) |
| [Delete File](actions/delete-file.md) | `DELETE /tools/files/{fileId}` | [docs](https://docs.autype.com/api-reference/developer-api/delete-a-file) |
| [Delete Temporary Image](actions/delete-temporary-image.md) | `DELETE /images/{imageId}` | [docs](https://docs.autype.com/api-reference/developer-api/delete-temporary-image) |
| [Download Bulk Render Output ZIP](actions/download-bulk-render-output-zip.md) | `GET /bulk-render/{bulkJobId}/download` | [docs](https://docs.autype.com/api-reference/developer-api/download-bulk-render-output-zip) |
| [Download File](actions/download-file.md) | `GET /tools/files/{fileId}/download` | [docs](https://docs.autype.com/api-reference/developer-api/download-a-file) |
| [Download Render Output File](actions/download-render-output-file.md) | `GET /render/{jobId}/download` | [docs](https://docs.autype.com/api-reference/developer-api/download-render-output-file) |
| [Get API Key Info](actions/get-api-key-info.md) | `GET /api-key/info` | [docs](https://docs.autype.com/api-reference/developer-api/api-key-info) |
| [Get Bulk Render Job Status](actions/get-bulk-render-job-status.md) | `GET /bulk-render/{bulkJobId}` | [docs](https://docs.autype.com/api-reference/developer-api/get-bulk-render-job-status) |
| [Get Document](actions/get-document.md) | `GET /documents/{documentId}` | [docs](https://docs.autype.com/api-reference/developer-api/get-document) |
| [Get Document Variables](actions/get-document-variables.md) | `GET /documents/{documentId}/variables` | [docs](https://docs.autype.com/api-reference/developer-api/get-document-variables) |
| [Get File Details](actions/get-file-details.md) | `GET /tools/files/{fileId}` | [docs](https://docs.autype.com/api-reference/developer-api/get-file-details) |
| [Get Render Job Status](actions/get-render-job-status.md) | `GET /render/{jobId}` | [docs](https://docs.autype.com/api-reference/developer-api/get-render-job-status) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://docs.autype.com/api-reference/developer-api/list-documents.md) |
| [List Files](actions/list-files.md) | `GET /tools/files` | [docs](https://docs.autype.com/api-reference/developer-api/list-files) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://docs.autype.com/api-reference/developer-api/list-projects) |
| [List Render Jobs](actions/list-render-jobs.md) | `GET /render` | [docs](https://docs.autype.com/api-reference/developer-api/list-render-jobs) |
| [List Temporary Images](actions/list-temporary-images.md) | `GET /images` | [docs](https://docs.autype.com/api-reference/developer-api/list-temporary-images) |
| [Merge PDFs](actions/merge-pdfs.md) | `POST /tools/pdf/merge` | [docs](https://docs.autype.com/api-reference/developer-api/merge-pdfs) |
| [Render Document](actions/render-document.md) | `POST /render` | [docs](https://docs.autype.com/api-reference/developer-api/render-document) |
| [Render Markdown](actions/render-markdown.md) | `POST /render/markdown` | [docs](https://docs.autype.com/api-reference/developer-api/render-markdown) |
| [Render Persistent Document](actions/render-persistent-document.md) | `POST /render/document/{documentId}` | [docs](https://docs.autype.com/api-reference/developer-api/render-persistent-document) |
| [Rotate PDF Pages](actions/rotate-pdf-pages.md) | `POST /tools/pdf/rotate` | [docs](https://docs.autype.com/api-reference/developer-api/rotate-pdf-pages) |
| [Split PDF](actions/split-pdf.md) | `POST /tools/pdf/split` | [docs](https://docs.autype.com/api-reference/developer-api/split-pdf) |
| [Upload File](actions/upload-file.md) | `POST /tools/files/upload` | [docs](https://docs.autype.com/api-reference/developer-api/upload-a-file) |
| [Upload Temporary Image](actions/upload-temporary-image.md) | `POST /images/upload` | [docs](https://docs.autype.com/api-reference/developer-api/upload-temporary-image) |
| [Validate Document JSON](actions/validate-document-json.md) | `POST /render/validate` | [docs](https://docs.autype.com/api-reference/developer-api/validate-document-json) |
| [Validate Markdown](actions/validate-markdown.md) | `POST /render/validate/markdown` | [docs](https://docs.autype.com/api-reference/developer-api/validate-markdown) |
