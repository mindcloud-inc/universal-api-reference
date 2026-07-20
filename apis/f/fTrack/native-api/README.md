# FTrack: Native API Reference

A consolidated summary of FTrack's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://developer.ftrack.com/api/
- **API base URL:** `{serverUrl}`

## Authentication

### API Key

Connect with an ftrack server URL, API user, and API key.

### Credentials

- **API Key:** `apiKey` · required
- **Server URL:** `serverUrl` · required · Workspace server URL, for example https://mycompany.ftrackapp.com
- **API User:** `apiUser` · required · Active ftrack username or email used with the API key.

Send these headers with each API request:

```http
Ftrack-User: <apiUser>
Ftrack-Api-Key: <apiKey>
```

[Official authentication documentation](https://developer.ftrack.com/api/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Permissions](actions/check-permissions.md) | `POST /api` | [docs](https://developer.ftrack.com/api/operations/permissions-api-permissions-permissions-post/) |
| [Complete Multipart Upload](actions/complete-multipart-upload.md) | `POST /api` | [docs](https://developer.ftrack.com/api/operations/complete-multipart-upload-api-complete-multipart-upload-completemultipartupload-post/) |
| [Convert Entity Type](actions/convert-entity-type.md) | `POST /api` | [docs](https://developer.ftrack.com/api/operations/convert-entity-api-convert-entity-convertentity-post/) |
| [Create Entity](actions/create-entity.md) | `POST /api` | [docs](https://developer.ftrack.com/api/operations/create-api-create-create-post/) |
| [CSV Import Delayed Job](actions/csv-import-delayed-job.md) | `POST /api` | [docs](https://developer.ftrack.com/api/operations/delayed-job-api-delayed-job-csvimportdelayedjob-post/) |
| [Delete Delayed Job](actions/delete-delayed-job.md) | `POST /api` | [docs](https://developer.ftrack.com/api/operations/delayed-job-api-delayed-job-deletedelayedjob-post/) |
| [Delete Entity](actions/delete-entity.md) | `POST /api` | [docs](https://developer.ftrack.com/api/operations/delete-api-delete-delete-post/) |
| [Encode Media](actions/encode-media.md) | `POST /api` | [docs](https://developer.ftrack.com/api/operations/encode-media-api-encode-media-encodemedia-post/) |
| [Export Review Session Feedback](actions/export-review-session-feedback.md) | `POST /api` | [docs](https://developer.ftrack.com/api/operations/delayed-job-api-delayed-job-exportreviewsessionfeedbackdelayedjob-post/) |
| [Generate Signed URL](actions/generate-signed-url.md) | `POST /api` | [docs](https://developer.ftrack.com/api/operations/generate-signed-url-api-generate-signed-url-generatesignedurl-post/) |
| [Get Storage Usage](actions/get-storage-usage.md) | `POST /api` | [docs](https://developer.ftrack.com/api/operations/storage-usage-api-storage-usage-storageusage-post/) |
| [Get Upload Metadata](actions/get-upload-metadata.md) | `POST /api` | [docs](https://developer.ftrack.com/api/operations/get-upload-metadata-api-get-upload-metadata-getuploadmetadata-post/) |
| [Parse Query](actions/parse-query.md) | `POST /api` | [docs](https://developer.ftrack.com/api/operations/parse-query-api-parse-query-parsequery-post/) |
| [Query Entities](actions/query-entities.md) | `POST /api` | [docs](https://developer.ftrack.com/api/operations/query-api-query-query-post/) |
| [Query Schemas](actions/query-schemas.md) | `POST /api` | [docs](https://developer.ftrack.com/api/operations/query-schemas-api-query-schemas-queryschemas-post/) |
| [Query Server Information](actions/query-server-information.md) | `POST /api` | [docs](https://developer.ftrack.com/api/operations/query-server-information-api-query-server-information-queryserverinformation-post/) |
| [Search Entities](actions/search-entities.md) | `POST /api` | [docs](https://developer.ftrack.com/api/operations/search-api-search-search-post/) |
| [Send Review Session Invite](actions/send-review-session-invite.md) | `POST /api` | [docs](https://developer.ftrack.com/api/operations/send-review-session-invite-api-send-review-session-invite-sendreviewsessioninvite-post/) |
| [Update Entity](actions/update-entity.md) | `POST /api` | [docs](https://developer.ftrack.com/api/operations/update-api-update-update-post/) |
