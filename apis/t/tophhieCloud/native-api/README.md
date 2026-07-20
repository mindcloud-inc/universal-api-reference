# Tophhie Cloud: Native API Reference

A consolidated summary of Tophhie Cloud's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.tophhie.cloud
- **OpenAPI specification:** https://api.tophhie.cloud/swagger/v1/swagger.json
- **API base URL:** `https://api.tophhie.cloud`

## Authentication

### No authentication

The selected public Tophhie Cloud API endpoints do not require authentication.

This API does not require request authentication.

[Official authentication documentation](https://api.tophhie.cloud)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check IP](actions/check-ip.md) | `GET /IPCheck` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [Check PDS TLS Domain](actions/check-pds-tls-domain.md) | `GET /pds/tls-check` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [Convert Entra ID](actions/convert-entra-id.md) | `GET /entra/convertid/{id}` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [Convert Entra IDs](actions/convert-entra-ids.md) | `POST /entra/convertid` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [Generate GUIDs](actions/generate-guids.md) | `GET /generate/guid` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [Generate Timestamp Ticks](actions/generate-timestamp-ticks.md) | `GET /generate/timestamp/ticks` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [Get Apple OS Version](actions/get-apple-os-version.md) | `GET /appleosversion/{appleDeviceModel}` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [Get Blog Info](actions/get-blog-info.md) | `GET /blog/info` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [Get Blog Post](actions/get-blog-post.md) | `GET /blog/posts/{id}` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [Get Domain](actions/get-domain.md) | `GET /domains/{domainName}` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [Get PDS Accessibility Score](actions/get-pds-accessibility-score.md) | `GET /pds/accessibilityScore/{did}` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [Get PDS Blob Storage Stats](actions/get-pds-blob-storage-stats.md) | `GET /pds/blobStorageStats` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [Get PDS Blob Storage Usage](actions/get-pds-blob-storage-usage.md) | `GET /pds/blobStorageUsageBytes` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [Get PDS Blob Storage Usage By DID](actions/get-pds-blob-storage-usage-by-did.md) | `GET /pds/blobStorageUsageBytes/{did}` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [Get PDS Bluesky Heatmap](actions/get-pds-bluesky-heatmap.md) | `GET /pds/blueskyHeatmap` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [Get PDS Uptime Stats](actions/get-pds-uptime-stats.md) | `GET /pds/uptimeStats` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [Get Redirect](actions/get-redirect.md) | `GET /redirect/{application}` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [Get Tenant Info](actions/get-tenant-info.md) | `GET /tenantinfo` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [List Blog Authors](actions/list-blog-authors.md) | `GET /blog/authors` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [List Blog Posts](actions/list-blog-posts.md) | `GET /blog/posts` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [List Domains](actions/list-domains.md) | `GET /domains` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [List M365 Message Center Blog Posts](actions/list-m365-message-center-blog-posts.md) | `GET /blog/posts/m365-message-center` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [List PDS Repositories](actions/list-pds-repositories.md) | `GET /pds/repos` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
| [Verify PDS Handle](actions/verify-pds-handle.md) | `GET /pds/verifyHandle` | [docs](https://api.tophhie.cloud/swagger/v1/swagger.json) |
