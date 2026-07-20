# <img src="https://images.mindcloud.co/apps/icons/id-rd1ph-qkj-logos_1775759708736.jpeg" alt="CINCEL logo" width="28" height="28"> CINCEL: Universal API

Create, sign, and manage documents and signature workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cINCEL/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cincel.digital
- **Vendor API docs:** https://docs.cincel.digital/v3/digital-signature

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List User Teams](actions/list-user-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/list-user-teams?connectionId=$CONNECTION_ID&limit=25&offset=0&user=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Audit Trail Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Download Audit Trail PDF](actions/download-audit-trail-pdf.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |

### Credit

| Action | Method | Description |
| --- | --- | --- |
| [Get Team Credits](actions/get-team-credits.md) | GET |  |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [List User Documents](actions/list-user-documents.md) | GET |  |

### Document Evidence Zip

| Action | Method | Description |
| --- | --- | --- |
| [Download Document Evidence ZIP](actions/download-document-evidence-zip.md) | GET |  |

### Document Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Download Original Document PDF](actions/download-original-document-pdf.md) | GET |  |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST |  |
| [Delete Folder](actions/delete-folder.md) | DELETE |  |
| [Get Folder](actions/get-folder.md) | GET |  |
| [List Folders](actions/list-folders.md) | GET |  |
| [Update Folder](actions/update-folder.md) | PUT |  |

### Invite

| Action | Method | Description |
| --- | --- | --- |
| [Create Document Invite](actions/create-document-invite.md) | POST |  |
| [Delete Document Invite](actions/delete-document-invite.md) | DELETE |  |
| [Get Document Invite](actions/get-document-invite.md) | GET |  |
| [List Document Invites](actions/list-document-invites.md) | GET |  |
| [Update Document Invite](actions/update-document-invite.md) | PUT |  |

### Invite Reminder

| Action | Method | Description |
| --- | --- | --- |
| [Send Invite Reminder](actions/send-invite-reminder.md) | GET |  |

### Signed Document Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Download Signed Document PDF](actions/download-signed-document-pdf.md) | GET |  |

### Signing Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Invite Signing Token](actions/get-invite-signing-token.md) | GET |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET |  |
| [List User Teams](actions/list-user-teams.md) | GET |  |

### Team Signed Documents Zip

| Action | Method | Description |
| --- | --- | --- |
| [Download Team Signed Documents ZIP](actions/download-team-signed-documents-zip.md) | GET |  |

### Timestamp Artifact

| Action | Method | Description |
| --- | --- | --- |
| [Get Timestamp Or Certificate Artifact](actions/get-timestamp-or-certificate-artifact.md) | GET |  |

### Token

| Action | Method | Description |
| --- | --- | --- |
| [Exchange OTP For JWT](actions/exchange-otp-for-jwt.md) | GET |  |
| [Request OTP](actions/request-otp.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Team Users](actions/list-team-users.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

