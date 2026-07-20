# <img src="https://images.mindcloud.co/apps/icons/one-deck_1774466427495.png" alt="OneDeck logo" width="28" height="28"> OneDeck: Universal API

Manage OneDeck boards, records, documents, and users

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oneDeck/latest
- **Category:** Productivity / Project Management
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.onedeck.com
- **Vendor API docs:** https://www.onedeck.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Upload Record Attachment](actions/upload-record-attachment.md) | POST | Uploads an attachment to a OneDeck board record. |

### Board

| Action | Method | Description |
| --- | --- | --- |
| [List Boards](actions/list-boards.md) | GET | Retrieves a list of boards from OneDeck. |

### Board Field

| Action | Method | Description |
| --- | --- | --- |
| [List Board Fields](actions/list-board-fields.md) | GET | Retrieves fields from a specific OneDeck board. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from OneDeck. |
| [List Documents](actions/list-documents.md) | GET | Retrieves a list of documents from OneDeck. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | POST | Creates a new record in a OneDeck board. |
| [Get Record](actions/get-record.md) | GET | Retrieves a record from a specific OneDeck board. |
| [List Records](actions/list-records.md) | GET | Retrieves records from a specific OneDeck board. |
| [Update Record](actions/update-record.md) | PUT | Updates an existing record in a OneDeck board. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Invite Share Studio User](actions/invite-share-studio-user.md) | POST | Invites a user to OneDeck Share Studio. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of users from OneDeck. |

