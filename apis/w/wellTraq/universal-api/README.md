# <img src="https://images.mindcloud.co/apps/icons/well-traq_1776449583755.png" alt="WellTraq logo" width="28" height="28"> WellTraq: Universal API

WellTraq through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wellTraq/latest
- **Category:** Support / Field Service
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.welltraq.com/
- **Vendor API docs:** https://www.welltraq.com/api/v1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Data Types](actions/list-data-types.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wellTraq/latest/actions/list-data-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Asset Measurement Type

| Action | Method | Description |
| --- | --- | --- |
| [Get All Asset Measurement Types For Asset](actions/get-all-asset-measurement-types-for-asset.md) | GET | Retrieves asset measurement types for an asset from WellTraq. |
| [Get Asset Measurement Type](actions/get-asset-measurement-type.md) | GET | Retrieves an asset measurement type from WellTraq. |
| [List Asset Measurement Types](actions/list-asset-measurement-types.md) | GET | Retrieves asset measurement types from WellTraq. |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Get Asset](actions/get-asset.md) | GET | Retrieves an asset from WellTraq. |
| [Get Asset Type](actions/get-asset-type.md) | GET | Retrieves an asset type from WellTraq. |
| [List Asset Types](actions/list-asset-types.md) | GET | Retrieves asset types from WellTraq. |
| [List Assets](actions/list-assets.md) | GET | Retrieves assets from WellTraq. |
| [List Assets By Last Modified Date](actions/list-assets-by-last-modified-date.md) | GET | Retrieves assets from WellTraq by last modified date. |

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Get Attachment](actions/get-attachment.md) | GET | Retrieves an attachment from WellTraq. |
| [Get Attachment Content](actions/get-attachment-content.md) | GET | Retrieves attachment content from WellTraq. |
| [Get Attachment File](actions/get-attachment-file.md) | GET | Retrieves an attachment file from WellTraq. |
| [List Attachments](actions/list-attachments.md) | GET | Retrieves attachments from WellTraq. |
| [List Attachments By Last Modified Date](actions/list-attachments-by-last-modified-date.md) | GET | Retrieves attachments from WellTraq by last modified date. |
| [List Attachments By Upload Date](actions/list-attachments-by-upload-date.md) | GET | Retrieves attachments from WellTraq by upload date. |

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [List Audit Log](actions/list-audit-log.md) | GET | Retrieves audit log entries from WellTraq. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Attachment Category](actions/get-attachment-category.md) | GET | Retrieves an attachment category from WellTraq. |
| [List Attachment Categories](actions/list-attachment-categories.md) | GET | Retrieves attachment categories from WellTraq. |

### Data Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Type](actions/get-data-type.md) | GET | Retrieves a data type from WellTraq. |
| [List Data Types](actions/list-data-types.md) | GET | Retrieves data types from WellTraq. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Get All Asset Form Types For Asset](actions/get-all-asset-form-types-for-asset.md) | GET | Retrieves asset form types for an asset from WellTraq. |
| [Get Asset Form Type](actions/get-asset-form-type.md) | GET | Retrieves an asset form type from WellTraq. |
| [Get Form Analytics Fields](actions/get-form-analytics-fields.md) | GET | Retrieves form analytics fields from WellTraq. |
| [Get Form Content](actions/get-form-content.md) | GET | Retrieves form content from WellTraq. |
| [Get Form File](actions/get-form-file.md) | GET | Retrieves a form file from WellTraq. |
| [List Asset Form Types](actions/list-asset-form-types.md) | GET | Retrieves asset form types from WellTraq. |
| [List Forms By Effective Date](actions/list-forms-by-effective-date.md) | GET | Retrieves forms from WellTraq by effective date. |
| [List Forms By Last Modified Date](actions/list-forms-by-last-modified-date.md) | GET | Retrieves forms from WellTraq by last modified date. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get Asset Group](actions/get-asset-group.md) | GET | Retrieves an asset group from WellTraq. |
| [List Asset Groups](actions/list-asset-groups.md) | GET | Retrieves asset groups from WellTraq. |
| [List Asset Groups By Last Modified Date](actions/list-asset-groups-by-last-modified-date.md) | GET | Retrieves asset groups from WellTraq by last modified date. |

