# <img src="https://images.mindcloud.co/apps/icons/images-29_1776983971092.png" alt="OKSign logo" width="28" height="28"> OKSign: Universal API

OKSign provides REST APIs for uploading documents, defining signing forms, sending notifications, retrieving signed documents and metadata, managing contacts, and checking account credits for OK!Sign e-signature workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oKSign/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://oksign.be/en/
- **Vendor API docs:** https://www.oksign.be/public/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Document Exists](actions/check-document-exists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oKSign/latest/actions/check-document-exists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Audit Trail

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Audit Trail](actions/retrieve-audit-trail.md) | GET | Retrieves an audit trail report from OKSign. |

### Briefcase

| Action | Method | Description |
| --- | --- | --- |
| [Create Briefcase](actions/create-briefcase.md) | POST | Creates a new briefcase in OKSign. |
| [Remove Briefcase](actions/remove-briefcase.md) | DELETE | Deletes a briefcase from OKSign. |
| [Retrieve Briefcase](actions/retrieve-briefcase.md) | GET | Retrieves a briefcase from OKSign. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Remove Contacts](actions/remove-contacts.md) | DELETE | Deletes contacts from OKSign. |
| [Retrieve Contacts](actions/retrieve-contacts.md) | GET | Retrieves contacts from OKSign. |
| [Upload Contacts](actions/upload-contacts.md) | POST | Creates or updates contacts in OKSign. |

### Credits

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Credits](actions/retrieve-credits.md) | GET | Retrieves credit details from OKSign. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Check Document Exists](actions/check-document-exists.md) | GET | Retrieves document existence details from OKSign. |
| [List Active Documents](actions/list-active-documents.md) | GET | Retrieves active documents from OKSign. |
| [List Signed Documents](actions/list-signed-documents.md) | GET | Retrieves signed documents from OKSign. |
| [Remove Document](actions/remove-document.md) | DELETE | Deletes a document from OKSign. |
| [Retrieve Document](actions/retrieve-document.md) | GET | Retrieves a document from OKSign. |
| [Upload Document](actions/upload-document.md) | POST | Creates a new document in OKSign. |

### Editor Express

| Action | Method | Description |
| --- | --- | --- |
| [Create Editor Express](actions/create-editor-express.md) | POST | Creates a new Editor Express session in OKSign. |
| [Remove Editor Express](actions/remove-editor-express.md) | DELETE | Deletes an Editor Express session from OKSign. |
| [Retrieve Editor Express](actions/retrieve-editor-express.md) | GET | Retrieves an Editor Express session from OKSign. |

### Email Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Remove Email Attachment](actions/remove-email-attachment.md) | DELETE | Deletes an email attachment from OKSign. |
| [Upload Email Attachment](actions/upload-email-attachment.md) | POST | Creates a new email attachment in OKSign. |

### Email Template

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Email Templates](actions/retrieve-email-templates.md) | GET | Retrieves email templates from OKSign. |

### Form Descriptor

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Form Descriptor](actions/retrieve-form-descriptor.md) | GET | Retrieves a form descriptor from OKSign. |
| [Upload Form Descriptor](actions/upload-form-descriptor.md) | POST | Creates a new form descriptor in OKSign. |

### Linked List

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Linked List](actions/retrieve-linked-list.md) | GET | Retrieves linked document identifiers from OKSign. |

### Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Metadata](actions/retrieve-metadata.md) | GET | Retrieves document metadata from OKSign. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Upload Notifications](actions/upload-notifications.md) | POST | Creates new notifications in OKSign. |

### Organization Token Info

| Action | Method | Description |
| --- | --- | --- |
| [Update Organization Token Info](actions/update-organization-token-info.md) | PUT | Updates organization token info in OKSign. |

### Sign Express

| Action | Method | Description |
| --- | --- | --- |
| [Create Sign Express](actions/create-sign-express.md) | POST | Creates a new Sign Express request in OKSign. |
| [Remove Sign Express](actions/remove-sign-express.md) | DELETE | Deletes a Sign Express request from OKSign. |
| [Retrieve Sign Express](actions/retrieve-sign-express.md) | GET | Retrieves a Sign Express request from OKSign. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Users](actions/retrieve-users.md) | GET | Retrieves users from OKSign. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhook errors from OKSign. |

