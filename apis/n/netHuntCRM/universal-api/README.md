# <img src="https://images.mindcloud.co/apps/icons/net-hunt-crm_1773685063816.png" alt="NetHunt CRM logo" width="28" height="28"> NetHunt CRM: Universal API

CRM for Gmail and Google Workspace that lets teams manage leads, contacts, deals, and customer communication through the NetHunt CRM API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/netHuntCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://nethunt.com
- **Vendor API docs:** https://nethunt.com/integration-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Request Credentials](actions/verify-request-credentials.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/verify-request-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Call Log

| Action | Method | Description |
| --- | --- | --- |
| [Create Record Call Log](actions/create-record-call-log.md) | POST | Creates a record call log in NetHunt CRM. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Record Comment](actions/create-record-comment.md) | POST | Creates a record comment in NetHunt CRM. |
| [Find Recently Created Record Comments](actions/find-recently-created-record-comments.md) | GET | Finds recently created record comments in NetHunt CRM. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [List Accessible Folders](actions/list-accessible-folders.md) | GET | Retrieves accessible folders from NetHunt CRM. |
| [List Writable Folders](actions/list-writable-folders.md) | GET | Retrieves writable folders from NetHunt CRM. |

### Folder Field

| Action | Method | Description |
| --- | --- | --- |
| [List Folder Fields](actions/list-folder-fields.md) | GET | Retrieves folder fields from NetHunt CRM. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Add Gmail Thread to Record](actions/add-gmail-thread-to-record.md) | PUT | Adds a Gmail thread to a NetHunt CRM record. |
| [Create Record](actions/create-record.md) | POST | Creates a new record in NetHunt CRM. |
| [Delete Record](actions/delete-record.md) | DELETE | Deletes an existing record from NetHunt CRM. |
| [Find Recently Created Records](actions/find-recently-created-records.md) | GET | Finds recently created records in NetHunt CRM. |
| [Find Recently Updated Records](actions/find-recently-updated-records.md) | GET | Finds recently updated records in NetHunt CRM. |
| [Find Records](actions/find-records.md) | GET | Finds records in NetHunt CRM by ID or query. |
| [Update Record](actions/update-record.md) | PUT | Updates an existing record in NetHunt CRM. |

### Record Change

| Action | Method | Description |
| --- | --- | --- |
| [Find Recent Record Changes](actions/find-recent-record-changes.md) | GET | Finds recent record changes in NetHunt CRM. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Verify Request Credentials](actions/verify-request-credentials.md) | GET | Verifies request credentials for NetHunt CRM. |

