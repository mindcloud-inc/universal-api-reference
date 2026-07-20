# <img src="https://images.mindcloud.co/apps/icons/scanova_1774362517441.png" alt="Scanova logo" width="28" height="28"> Scanova: Universal API

Generate, manage, and analyze QR codes programmatically with Scanova, including QR code management, lead lists, user access, and analytics.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scanova/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://scanova.io
- **Vendor API docs:** https://docs.scanova.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Account Statistics](actions/account-statistics.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scanova/latest/actions/account-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Accountstatistics

| Action | Method | Description |
| --- | --- | --- |
| [Account Statistics](actions/account-statistics.md) | GET |  |

### Leadlist

| Action | Method | Description |
| --- | --- | --- |
| [Delete Lead List](actions/delete-lead-list.md) | DELETE |  |
| [List Lead Lists](actions/list-lead-lists.md) | GET |  |
| [Retrieve Lead List](actions/retrieve-lead-list.md) | GET |  |
| [Update Lead List](actions/update-lead-list.md) | PUT |  |

### Qranalytics

| Action | Method | Description |
| --- | --- | --- |
| [Get QR Code Analytics](actions/get-qr-code-analytics.md) | GET |  |

### Qranalyticsexport

| Action | Method | Description |
| --- | --- | --- |
| [Export Analytics Data](actions/export-analytics-data.md) | GET |  |

### Qrcategory

| Action | Method | Description |
| --- | --- | --- |
| [Get QR Code Categories](actions/get-qr-code-categories.md) | GET |  |

### Qrcode

| Action | Method | Description |
| --- | --- | --- |
| [Attach Or Detach Lead List](actions/attach-or-detach-lead-list.md) | PUT |  |
| [Create QR Code](actions/create-qr-code.md) | POST |  |
| [Delete QR Code](actions/delete-qr-code.md) | DELETE |  |
| [Download QR Code](actions/download-qr-code.md) | GET |  |
| [Download QR Code (Printable)](actions/download-qr-code-printable.md) | GET |  |
| [Get QR Code List](actions/get-qr-code-list.md) | GET |  |
| [Update QR Code](actions/update-qr-code.md) | PUT |  |
| [Validate QR Code Info Data](actions/validate-qr-code-info-data.md) | GET |  |

### Qrrawscanexport

| Action | Method | Description |
| --- | --- | --- |
| [Export Raw Scan Data](actions/export-raw-scan-data.md) | GET |  |

### Shareduser

| Action | Method | Description |
| --- | --- | --- |
| [Add New User](actions/add-new-user.md) | POST |  |
| [Get User Details](actions/get-user-details.md) | GET |  |
| [Get User List](actions/get-user-list.md) | GET |  |
| [Remove User](actions/remove-user.md) | DELETE |  |
| [Update User Role](actions/update-user-role.md) | PUT |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST |  |
| [Delete Tag](actions/delete-tag.md) | DELETE |  |
| [Get Tags](actions/get-tags.md) | GET |  |
| [Update Tag](actions/update-tag.md) | PUT |  |

### Trashqrcode

| Action | Method | Description |
| --- | --- | --- |
| [Get Trash QR Codes](actions/get-trash-qr-codes.md) | GET |  |
| [Permanently Delete QR Code](actions/permanently-delete-qr-code.md) | DELETE |  |
| [Restore QR Code From Trash](actions/restore-qr-code-from-trash.md) | PUT |  |

### Userrole

| Action | Method | Description |
| --- | --- | --- |
| [Get User Roles List](actions/get-user-roles-list.md) | GET |  |

