# Atlas AI Revenue Engine: Native API Reference

A consolidated summary of Atlas AI Revenue Engine's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.youratlas.com/what-can-you-build-with-the-atlas-api-2063751m0
- **API base URL:** `https://api.youratlas.com/v1/api`

## Authentication

### API Key

Use your Atlas API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
api-key: <apiKey>
```

[Official authentication documentation](https://apidocs.youratlas.com/api-keys-985594m0.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `value`.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Knowledge Base File to Collection](actions/add-knowledge-base-file-to-collection.md) | `POST /knowledgebase/:id/tag` | [docs](https://apidocs.youratlas.com/add-file-to-collection-26917878e0) |
| [Attach Knowledge Base File to Campaign](actions/attach-knowledge-base-file-to-campaign.md) | `POST /knowledgebase/:campaignId/:rowKey` | [docs](https://apidocs.youratlas.com/attach-file-to-campaign-26917876e0) |
| [Create Scheduled Call](actions/create-scheduled-call.md) | `POST /campaign/createschedule` | [docs](https://apidocs.youratlas.com/create-scheduled-call-26754250e0) |
| [Delete Call Record](actions/delete-call-record.md) | `DELETE /call/:id` | [docs](https://apidocs.youratlas.com/delete-call-record-26754247e0) |
| [Delete Campaign](actions/delete-campaign.md) | `DELETE /campaign/:id` | [docs](https://apidocs.youratlas.com/delete-campaign-26754246e0) |
| [Delete Knowledge Base File](actions/delete-knowledge-base-file.md) | `DELETE /knowledgebase` | [docs](https://apidocs.youratlas.com/delete-knowledge-file-26917874e0) |
| [Detach Knowledge Base File from Campaign](actions/detach-knowledge-base-file-from-campaign.md) | `DELETE /knowledgebase/:campaignId/:rowKey` | [docs](https://apidocs.youratlas.com/detach-file-from-campaign-26917877e0) |
| [Get Call Record](actions/get-call-record.md) | `GET /call/:id` | [docs](https://apidocs.youratlas.com/get-call-record-details-26754277e0) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaign/:id` | [docs](https://apidocs.youratlas.com/get-campaign-by-id-26105299e0) |
| [Get Campaign Statistics](actions/get-campaign-statistics.md) | `GET /call/stats/:id` | [docs](https://apidocs.youratlas.com/get-campaign-statistics-26105303e0) |
| [List Call Bookings](actions/list-call-bookings.md) | `GET /campaign/:campaignId/bookings/callId/:callId` | [docs](https://apidocs.youratlas.com/get-bookings-for-call-26754252e0) |
| [List Call Records](actions/list-call-records.md) | `GET /call` | [docs](https://apidocs.youratlas.com/get-call-records-26753535e0) |
| [List Campaign Bookings](actions/list-campaign-bookings.md) | `GET /campaign/:campaignId/bookings` | [docs](https://apidocs.youratlas.com/get-bookings-for-campaign-26754251e0) |
| [List Campaign Knowledge Base Files](actions/list-campaign-knowledge-base-files.md) | `GET /knowledgebase/:campaignId` | [docs](https://apidocs.youratlas.com/get-knowledge-files-for-campaign-26917875e0) |
| [List Campaign Overview Statistics](actions/list-campaign-overview-statistics.md) | `GET /call/stats` | [docs](https://apidocs.youratlas.com/get-all-campaigns-overview-statistics-26105302e0) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaign` | [docs](https://apidocs.youratlas.com/get-all-campaigns-26105298e0) |
| [List Knowledge Base File Linked Campaigns](actions/list-knowledge-base-file-linked-campaigns.md) | `GET /knowledgebase/:rowKey/campaigns` | [docs](https://apidocs.youratlas.com/get-file-linked-campaigns-26917880e0) |
| [List Knowledge Base Files](actions/list-knowledge-base-files.md) | `GET /knowledgebase` | [docs](https://apidocs.youratlas.com/get-all-knowledge-base-files-26917873e0) |
| [List Scheduled Calls](actions/list-scheduled-calls.md) | `GET /call/scheduled/:id` | [docs](https://apidocs.youratlas.com/get-scheduled-calls-26754249e0) |
| [Remove Knowledge Base File from Collection](actions/remove-knowledge-base-file-from-collection.md) | `DELETE /knowledgebase/:rowKey/tag/:collectionName` | [docs](https://apidocs.youratlas.com/remove-file-from-collection-26917879e0) |
| [Set Campaign Status](actions/set-campaign-status.md) | `PUT /campaign/:campaignId/status` | [docs](https://apidocs.youratlas.com/set-campaign-status-26124567e0) |
| [Update Campaign](actions/update-campaign.md) | `PUT /campaign/:id` | [docs](https://apidocs.youratlas.com/update-campaign-26754245e0) |
| [Upload Knowledge Base File](actions/upload-knowledge-base-file.md) | `POST /knowledgebase/upload` | [docs](https://apidocs.youratlas.com/upload-knowledge-file-26917881e0) |
| [Upload Knowledge from URL](actions/upload-knowledge-from-url.md) | `POST /knowledgebase/knowledge-extract` | [docs](https://apidocs.youratlas.com/upload-knowledge-from-url-26917882e0) |
