# <img src="https://images.mindcloud.co/apps/icons/right-signature_1774036658691.png" alt="RightSignature logo" width="28" height="28"> RightSignature: Universal API

Send, sign, and manage documents, reusable templates, and signature workflows with RightSignature.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rightSignature/latest
- **Category:** Content & Files / Storage
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sharefile.com/rightsignature
- **Vendor API docs:** https://api.rightsignature.com/documentation/getting_started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Me](actions/get-me.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/get-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Request OAuth Access Token](actions/request-oauth-access-token.md) | POST | Requests a RightSignature OAuth access token. |
| [Revoke OAuth Access Token](actions/revoke-oauth-access-token.md) | POST | Revokes a RightSignature OAuth access token. |

### Archived Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Archived Document By Original GUID](actions/get-archived-document-by-original-guid.md) | GET | Retrieves an archived RightSignature document by original GUID. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Document](actions/get-document.md) | GET | Retrieves a specific document from RightSignature. |
| [List Documents](actions/list-documents.md) | GET | Retrieves available documents from your RightSignature account. |
| [Share Document](actions/share-document.md) | POST | Shares a document in RightSignature with new recipients. |
| [Update Document PIN](actions/update-document-pin.md) | PUT | Updates the PIN for an existing RightSignature document. |
| [Update Document Tags](actions/update-document-tags.md) | POST | Replaces tags on an existing RightSignature document. |
| [Void Document](actions/void-document.md) | POST | Voids an existing document in RightSignature. |

### Oauth Authorization

| Action | Method | Description |
| --- | --- | --- |
| [Request OAuth Authorization Code](actions/request-oauth-authorization-code.md) | GET | Requests a RightSignature OAuth authorization code. |

### Reusable Template

| Action | Method | Description |
| --- | --- | --- |
| [Delete Reusable Template](actions/delete-reusable-template.md) | DELETE | Deletes a reusable template from RightSignature. |
| [Embed Document From Reusable Template](actions/embed-document-from-reusable-template.md) | POST | Creates an embeddable document from a RightSignature reusable template. |
| [Get Reusable Template](actions/get-reusable-template.md) | GET | Retrieves a specific reusable template from RightSignature. |
| [List Reusable Templates](actions/list-reusable-templates.md) | GET | Retrieves reusable templates from your RightSignature account. |
| [Merge And Send Document](actions/merge-and-send-document.md) | POST | Creates and sends a document from a RightSignature reusable template. |
| [Prepare Document From Reusable Template](actions/prepare-document-from-reusable-template.md) | POST | Prepares a document from a RightSignature reusable template. |
| [Send Document From Reusable Template](actions/send-document-from-reusable-template.md) | POST | Sends a document from a RightSignature reusable template. |

### Reusable Template Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add Or Update Reusable Template Tags](actions/add-or-update-reusable-template-tags.md) | PUT | Adds or updates tags on a RightSignature reusable template. |
| [Delete Reusable Template Tag](actions/delete-reusable-template-tag.md) | DELETE | Deletes a tag from a RightSignature reusable template. |
| [List Reusable Template Tags](actions/list-reusable-template-tags.md) | GET | Retrieves tags for a RightSignature reusable template. |
| [Replace Reusable Template Tags](actions/replace-reusable-template-tags.md) | POST | Replaces tags on a RightSignature reusable template. |

### Sending Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Sending Request](actions/create-sending-request.md) | POST | Creates a RightSignature sending request for a one-off document. |
| [Get Sending Request](actions/get-sending-request.md) | GET | Retrieves a RightSignature sending request status. |
| [Mark Sending Request Uploaded](actions/mark-sending-request-uploaded.md) | POST | Marks a RightSignature sending request upload as complete. |

### Signer

| Action | Method | Description |
| --- | --- | --- |
| [Send Signer Reminder](actions/send-signer-reminder.md) | POST | Sends a reminder email to a pending RightSignature signer. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Me](actions/get-me.md) | GET | Retrieves the authenticated RightSignature user profile. |

