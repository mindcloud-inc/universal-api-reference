# EyeLevel.ai: Native API Reference

A consolidated summary of EyeLevel.ai's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.eyelevel.ai/documentation/fundamentals/welcome
- **API base URL:** `https://api.groundx.ai/api/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.eyelevel.ai/documentation/fundamentals/api-concepts)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Bucket To Group](actions/add-bucket-to-group.md) | `POST /group/:groupId/bucket/:bucketId` | [docs](https://docs.eyelevel.ai/reference/api-reference/groups/add-bucket) |
| [Crawl Website](actions/crawl-website.md) | `POST /ingest/documents/website` | [docs](https://docs.eyelevel.ai/reference/api-reference/documents/crawl-website) |
| [Create Bucket](actions/create-bucket.md) | `POST /bucket` | [docs](https://docs.eyelevel.ai/reference/api-reference/buckets/create) |
| [Create Group](actions/create-group.md) | `POST /group` | [docs](https://docs.eyelevel.ai/reference/api-reference/groups/create) |
| [Delete Bucket](actions/delete-bucket.md) | `DELETE /bucket/:bucketId` | [docs](https://docs.eyelevel.ai/reference/api-reference/buckets/delete) |
| [Delete Group](actions/delete-group.md) | `DELETE /group/:groupId` | [docs](https://docs.eyelevel.ai/reference/api-reference/groups/delete) |
| [Get Bucket](actions/get-bucket.md) | `GET /bucket/:bucketId` | [docs](https://docs.eyelevel.ai/reference/api-reference/buckets/get) |
| [Get Customer](actions/get-customer.md) | `GET /customer` | [docs](https://docs.eyelevel.ai/reference/api-reference/customer/get) |
| [Get Group](actions/get-group.md) | `GET /group/:groupId` | [docs](https://docs.eyelevel.ai/reference/api-reference/groups/get) |
| [Get Health Status](actions/get-health-status.md) | `GET /health/:service` | [docs](https://docs.eyelevel.ai/reference/api-reference/health/get) |
| [Get Processing Status](actions/get-processing-status.md) | `GET /ingest/:processId` | [docs](https://docs.eyelevel.ai/reference/api-reference/documents/get-processing-status-by-id) |
| [List Buckets](actions/list-buckets.md) | `GET /bucket` | [docs](https://docs.eyelevel.ai/reference/api-reference/buckets/) |
| [List Documents](actions/list-documents.md) | `GET /ingest/documents` | [docs](https://docs.eyelevel.ai/reference/api-reference/documents/list) |
| [List Groups](actions/list-groups.md) | `GET /group` | [docs](https://docs.eyelevel.ai/reference/api-reference/groups/list) |
| [List Health Statuses](actions/list-health-statuses.md) | `GET /health` | [docs](https://docs.eyelevel.ai/reference/api-reference/health/list) |
| [List Ingest Processes](actions/list-ingest-processes.md) | `GET /ingest` | [docs](https://docs.eyelevel.ai/reference/api-reference/documents/get-processes) |
| [Lookup Documents](actions/lookup-documents.md) | `GET /ingest/documents/:id` | [docs](https://docs.eyelevel.ai/reference/api-reference/documents/lookup) |
| [Remove Bucket From Group](actions/remove-bucket-from-group.md) | `DELETE /group/:groupId/bucket/:bucketId` | [docs](https://docs.eyelevel.ai/reference/api-reference/groups/remove-bucket) |
| [Update Bucket](actions/update-bucket.md) | `PUT /bucket/:bucketId` | [docs](https://docs.eyelevel.ai/reference/api-reference/buckets/update) |
| [Update Group](actions/update-group.md) | `PUT /group/:groupId` | [docs](https://docs.eyelevel.ai/reference/api-reference/groups/update) |
