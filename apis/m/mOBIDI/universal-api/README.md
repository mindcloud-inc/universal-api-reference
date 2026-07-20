# <img src="https://images.mindcloud.co/apps/icons/m-obidi_1775060318349.png" alt="MOBIDI logo" width="28" height="28"> MOBIDI: Universal API

Manage mobile teams, forms, reports, and dashboards

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mOBIDI/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mobidi.com/
- **Vendor API docs:** https://destek.dece.com.tr/space/PAR/1308360709/Mobidi+Office+API+Documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Query Record Counts](actions/query-record-counts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/query-record-counts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Upload Attachment](actions/upload-attachment.md) | POST | Uploads an attachment to a MOBIDI record. |

### Dashboard

| Action | Method | Description |
| --- | --- | --- |
| [List Dashboards](actions/list-dashboards.md) | GET | Retrieves available dashboards from MOBIDI. |

### Layer

| Action | Method | Description |
| --- | --- | --- |
| [Save Layer](actions/save-layer.md) | POST | Creates or updates a layer in MOBIDI. |

### Login Provider

| Action | Method | Description |
| --- | --- | --- |
| [List Allowed Login Providers](actions/list-allowed-login-providers.md) | GET | Retrieves allowed login providers from MOBIDI. |

### Mobidi Folder

| Action | Method | Description |
| --- | --- | --- |
| [Get Mobidi Folder Path](actions/get-mobidi-folder-path.md) | GET | Retrieves the configured MOBIDI folder path. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Generate Image Thumbnail](actions/generate-image-thumbnail.md) | PUT | Generates an image thumbnail for a MOBIDI attachment. |
| [Get Attachment](actions/get-attachment.md) | GET | Retrieves an attachment from a MOBIDI record. |
| [Get New Record Template](actions/get-new-record-template.md) | GET | Retrieves a new record template from MOBIDI. |
| [Get Next Or Previous Record](actions/get-next-or-previous-record.md) | GET | Retrieves the next or previous record in MOBIDI. |
| [Get Record Change Log](actions/get-record-change-log.md) | GET | Retrieves a record change log from MOBIDI. |
| [Get Record Detail](actions/get-record-detail.md) | GET | Retrieves detailed record data from MOBIDI. |
| [Rotate Image](actions/rotate-image.md) | PUT | Rotates an image attachment in MOBIDI. |
| [Update Annotations](actions/update-annotations.md) | PUT | Updates annotations on a MOBIDI record. |

### Query Counter

| Action | Method | Description |
| --- | --- | --- |
| [Query Record Counts](actions/query-record-counts.md) | GET | Retrieves record counts for a MOBIDI query. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Record](actions/create-or-update-record.md) | POST | Creates or updates a record in MOBIDI. |
| [Query Records](actions/query-records.md) | GET | Retrieves records from a MOBIDI query. |

### Saved Query

| Action | Method | Description |
| --- | --- | --- |
| [List Saved Queries](actions/list-saved-queries.md) | GET | Retrieves saved user queries from MOBIDI. |
| [Save Query For User](actions/save-query-for-user.md) | POST | Saves a query for a MOBIDI user. |
| [Set Default Query](actions/set-default-query.md) | PUT | Sets the default query in MOBIDI. |
| [Update Or Delete Saved Query](actions/update-or-delete-saved-query.md) | PUT | Updates or deletes a saved query in MOBIDI. |

### Sync Health

| Action | Method | Description |
| --- | --- | --- |
| [Check Sync Health](actions/check-sync-health.md) | GET | Retrieves sync health details from MOBIDI. |

### Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Token](actions/create-token.md) | POST | Creates an access token in MOBIDI. |
| [Create Token For User](actions/create-token-for-user.md) | POST | Creates a user access token in MOBIDI. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List All Layers](actions/list-all-layers.md) | GET | Retrieves all layers from MOBIDI. |

