# Filestack: Native API Reference

A consolidated summary of Filestack's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://www.filestack.com/docs/api/file/
- **API base URL:** `https://www.filestackapi.com/api`

## Authentication

### API Key

Use your Filestack API key for File API requests. Security-sensitive operations may also require per-request policy and signature values generated from your Filestack app secret on your backend.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.filestack.com/docs/api/file/)

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | `DELETE /file/:handle` | [docs](https://www.filestack.com/docs/api/file/#delete) |
| [Get File Metadata](actions/get-file-metadata.md) | `GET /file/:handle/metadata` | [docs](https://www.filestack.com/docs/api/file/#metadata) |
| [Get Workflow Status](actions/get-workflow-status.md) | `GET https://cdn.filestackcontent.com/{{credentials.apiKey}}/security=p\:{{policy}},s\:{{signature}}/workflow_status=job_id\:{{jobId}}` | [docs](https://www.filestack.com/docs/api/workflows_api/#workflow-status) |
| [Run Workflow On File](actions/run-workflow-on-file.md) | `GET https://cdn.filestackcontent.com/security=p\:{{policy}},s\:{{signature}}/run_workflow=id\:{{workflowId}}/{{handle}}` | [docs](https://www.filestack.com/docs/api/workflows_api/#run-workflow) |
| [Store File From URL](actions/store-file-from-url.md) | `POST /store/S3` | [docs](https://www.filestack.com/docs/api/file/#store) |
