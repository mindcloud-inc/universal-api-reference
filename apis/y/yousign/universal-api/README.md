# <img src="https://images.mindcloud.co/apps/icons/yousign_1773538150579.png" alt="Yousign logo" width="28" height="28"> Yousign: Universal API

Send, track, and manage Yousign signature requests and signers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/yousign/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://yousign.com
- **Vendor API docs:** https://developers.yousign.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Default Workspace](actions/get-default-workspace.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yousign/latest/actions/get-default-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Yousign. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Yousign. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Yousign. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Yousign. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Add Signature Request Document](actions/add-signature-request-document.md) | POST | Adds a document to a Yousign signature request. |
| [Download Signature Request Documents](actions/download-signature-request-documents.md) | GET | Downloads documents from a Yousign signature request. |
| [List Signature Request Documents](actions/list-signature-request-documents.md) | GET | Retrieves documents from a Yousign signature request. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Create Label](actions/create-label.md) | POST | Creates a new label in Yousign. |
| [Get Label](actions/get-label.md) | GET | Retrieves a label from Yousign. |
| [List Labels](actions/list-labels.md) | GET | Retrieves labels from Yousign. |

### Signature Requests

| Action | Method | Description |
| --- | --- | --- |
| [Activate Signature Request](actions/activate-signature-request.md) | PUT | Activates a signature request in Yousign. |
| [Cancel Signature Request](actions/cancel-signature-request.md) | PUT | Cancels a signature request in Yousign. |
| [Create Signature Request](actions/create-signature-request.md) | POST | Creates a new signature request in Yousign. |
| [Fetch Signature Request](actions/fetch-signature-request.md) | GET | Retrieves a signature request from Yousign. |
| [List Signature Requests](actions/list-signature-requests.md) | GET | Retrieves signature requests from Yousign. |
| [Update Signature Request](actions/update-signature-request.md) | PUT | Updates an existing signature request in Yousign. |

### Signer

| Action | Method | Description |
| --- | --- | --- |
| [Add Signature Request Signer](actions/add-signature-request-signer.md) | POST | Creates a signer for a Yousign signature request. |
| [List Signature Request Signers](actions/list-signature-request-signers.md) | GET | Retrieves signers from a Yousign signature request. |
| [Send Signer Reminder](actions/send-signer-reminder.md) | PUT | Sends a reminder to a Yousign signer. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Yousign. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Yousign. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Yousign. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Default Workspace](actions/get-default-workspace.md) | GET | Retrieves the default workspace from Yousign. |

