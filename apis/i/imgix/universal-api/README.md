# <img src="https://images.mindcloud.co/apps/icons/imgix-icon-square_1776185662136.png" alt="imgix logo" width="28" height="28"> imgix: Universal API

Programmatic access to the imgix Management API for sources, assets, reports, purges, and upload-session workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/imgix/latest
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.imgix.com
- **Vendor API docs:** https://docs.imgix.com/en-US/apis/management/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sources](actions/list-sources.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imgix/latest/actions/list-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [Add Asset From Origin](actions/add-asset-from-origin.md) | POST | Adds an asset from origin to imgix. |
| [Get Asset](actions/get-asset.md) | GET | Retrieves an asset from an imgix source. |
| [List Assets](actions/list-assets.md) | GET | Retrieves assets from an imgix source. |
| [Overwrite Uploaded Asset](actions/overwrite-uploaded-asset.md) | PUT | Overwrites an uploaded asset in an imgix source. |
| [Publish Asset](actions/publish-asset.md) | PUT | Publishes an asset in imgix. |
| [Refresh Asset](actions/refresh-asset.md) | PUT | Refreshes an asset in imgix from origin. |
| [Unpublish Asset](actions/unpublish-asset.md) | DELETE | Unpublishes an asset in imgix. |
| [Update Asset](actions/update-asset.md) | PUT | Updates an asset in imgix. |
| [Upload Asset](actions/upload-asset.md) | POST | Uploads an asset to an imgix source. |

### Purge

| Action | Method | Description |
| --- | --- | --- |
| [Create Purge](actions/create-purge.md) | DELETE | Purges an asset from the imgix cache. |
| [Purge Sub-image](actions/purge-sub-image.md) | DELETE | Purges a sub-image from the imgix cache. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Report](actions/get-report.md) | GET | Retrieves a report from imgix. |
| [List Reports](actions/list-reports.md) | GET | Retrieves reports from imgix. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [Create Source](actions/create-source.md) | POST | Creates a source in imgix. |
| [Get Source](actions/get-source.md) | GET | Retrieves a source from imgix. |
| [List Sources](actions/list-sources.md) | GET | Retrieves sources from imgix. |
| [Update Source](actions/update-source.md) | PUT | Updates a source in imgix. |

### Upload Session

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Upload Session](actions/cancel-upload-session.md) | DELETE | Cancels an upload session in imgix. |
| [Close Upload Session](actions/close-upload-session.md) | PUT |  |
| [Get Upload Session](actions/get-upload-session.md) | GET | Retrieves an upload session from imgix. |
| [Open Upload Session](actions/open-upload-session.md) | POST | Opens an upload session in imgix. |

