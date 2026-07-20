# imgix: Native API Reference

A consolidated summary of imgix's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://docs.imgix.com/en-US/apis/management/overview
- **OpenAPI specification:** https://docs.imgix.com/en-US/apis/management/overview
- **API base URL:** `https://api.imgix.com/api/v1`

## Authentication

### imgix API Key

Use an imgix Management API key. The key is sent as Authorization: Bearer <api-key>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.imgix.com/en-US/apis/management/overview)

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Asset From Origin](actions/add-asset-from-origin.md) | `POST sources/:sourceId/assets/add/:originPath` | [docs](https://docs.imgix.com/en-US/apis/management/assets) |
| [Cancel Upload Session](actions/cancel-upload-session.md) | `DELETE sources/:sourceId/upload-sessions/cancel/:sessionId` | [docs](https://docs.imgix.com/en-US/apis/management/assets) |
| [Close Upload Session](actions/close-upload-session.md) | `POST sources/:sourceId/upload-sessions/:sessionId` | [docs](https://docs.imgix.com/en-US/apis/management/assets) |
| [Create Purge](actions/create-purge.md) | `POST purge` | [docs](https://docs.imgix.com/en-US/apis/management/purges) |
| [Create Source](actions/create-source.md) | `POST sources` | [docs](https://docs.imgix.com/en-US/apis/management/sources) |
| [Get Asset](actions/get-asset.md) | `GET sources/:sourceId/assets/:originPath` | [docs](https://docs.imgix.com/en-US/apis/management/assets) |
| [Get Report](actions/get-report.md) | `GET reports/:reportId` | [docs](https://docs.imgix.com/en-US/apis/management/reports) |
| [Get Source](actions/get-source.md) | `GET sources/:sourceId` | [docs](https://docs.imgix.com/en-US/apis/management/sources) |
| [Get Upload Session](actions/get-upload-session.md) | `GET sources/:sourceId/upload-sessions/status/:sessionId` | [docs](https://docs.imgix.com/en-US/apis/management/assets) |
| [List Assets](actions/list-assets.md) | `GET sources/:sourceId/assets` | [docs](https://docs.imgix.com/en-US/apis/management/assets) |
| [List Reports](actions/list-reports.md) | `GET reports` | [docs](https://docs.imgix.com/en-US/apis/management/reports) |
| [List Sources](actions/list-sources.md) | `GET sources` | [docs](https://docs.imgix.com/en-US/apis/management/sources) |
| [Open Upload Session](actions/open-upload-session.md) | `POST sources/:sourceId/upload-sessions/create/:originPath` | [docs](https://docs.imgix.com/en-US/apis/management/assets) |
| [Overwrite Uploaded Asset](actions/overwrite-uploaded-asset.md) | `POST sources/:sourceId/upload/:originPath` | [docs](https://docs.imgix.com/en-US/apis/management/assets) |
| [Publish Asset](actions/publish-asset.md) | `POST publish` | [docs](https://docs.imgix.com/en-US/apis/management/assets) |
| [Purge Sub-image](actions/purge-sub-image.md) | `POST purge` | [docs](https://docs.imgix.com/en-US/apis/management/purges) |
| [Refresh Asset](actions/refresh-asset.md) | `POST sources/:sourceId/assets/refresh/:originPath` | [docs](https://docs.imgix.com/en-US/apis/management/assets) |
| [Unpublish Asset](actions/unpublish-asset.md) | `POST unpublish` | [docs](https://docs.imgix.com/en-US/apis/management/assets) |
| [Update Asset](actions/update-asset.md) | `PATCH sources/:sourceId/assets/:originPath` | [docs](https://docs.imgix.com/en-US/apis/management/assets) |
| [Update Source](actions/update-source.md) | `PATCH sources/:sourceId` | [docs](https://docs.imgix.com/en-US/apis/management/sources) |
| [Upload Asset](actions/upload-asset.md) | `POST sources/:sourceId/upload/:originPath` | [docs](https://docs.imgix.com/en-US/apis/management/assets) |
