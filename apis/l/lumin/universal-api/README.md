# <img src="https://images.mindcloud.co/apps/icons/idbp7tbkv-g-logos_1775072725307.png" alt="Lumin logo" width="28" height="28"> Lumin: Universal API

Lumin: Create, edit, sign, and manage documents and agreements

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lumin/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.luminpdf.com
- **Vendor API docs:** https://developers.luminpdf.com/api/lumin-api-reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Information](actions/get-user-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lumin/latest/actions/get-user-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST |  |

### Signature Request

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Signature Request](actions/cancel-signature-request.md) | DELETE |  |
| [Get Signature Request](actions/get-signature-request.md) | GET |  |
| [Send Reminder Emails](actions/send-reminder-emails.md) | PUT |  |
| [Send Signature Request](actions/send-signature-request.md) | POST |  |
| [Update Signature Request](actions/update-signature-request.md) | PUT |  |

### Signature Request File

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET |  |
| [Download File As File URL](actions/download-file-as-file-url.md) | GET |  |
| [Get Signature Request File](actions/get-signature-request-file.md) | GET |  |

### Signing Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Signing Link](actions/get-signing-link.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Information](actions/get-user-information.md) | GET |  |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace Information](actions/get-workspace-information.md) | GET |  |

### Workspace Member

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Members](actions/list-workspace-members.md) | GET |  |

