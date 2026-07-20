# <img src="https://images.mindcloud.co/apps/icons/fuse-desk_1774977840447.png" alt="FuseDesk logo" width="28" height="28"> FuseDesk: Universal API

Manage support cases, emails, contacts, chats, and departments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fuseDesk/latest
- **Category:** Support / Ticketing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fusedesk.com/
- **Vendor API docs:** https://www.fusedesk.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Active Departments](actions/list-active-departments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/list-active-departments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Case

| Action | Method | Description |
| --- | --- | --- |
| [Apply Case Tag](actions/apply-case-tag.md) | PUT | Applies a tag to an existing FuseDesk case. |
| [Bulk Update Cases](actions/bulk-update-cases.md) | PUT | Updates multiple existing cases in FuseDesk. |
| [Create Case](actions/create-case.md) | POST | Creates a new case in FuseDesk. |
| [Get Case](actions/get-case.md) | GET | Retrieves a case and its history from FuseDesk. |
| [Remove Case Tag](actions/remove-case-tag.md) | PUT | Removes a tag from an existing FuseDesk case. |
| [Search Cases](actions/search-cases.md) | GET | Finds cases in FuseDesk by matching search filters. |
| [Snooze Case](actions/snooze-case.md) | PUT | Snoozes an existing FuseDesk case until a later time. |
| [Update Case](actions/update-case.md) | PUT | Updates an existing case in FuseDesk. |

### Case Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Disable Case Feedback](actions/disable-case-feedback.md) | PUT | Disables case feedback requests in FuseDesk. |
| [Enable Case Feedback](actions/enable-case-feedback.md) | PUT | Enables case feedback requests in FuseDesk. |
| [Get Case Feedback Data](actions/get-case-feedback-data.md) | GET | Retrieves feedback data for an existing FuseDesk case. |
| [Request Case Feedback Now](actions/request-case-feedback-now.md) | PUT | Requests case feedback immediately in FuseDesk. |

### Case Note

| Action | Method | Description |
| --- | --- | --- |
| [Add Case Note](actions/add-case-note.md) | POST | Creates a note on an existing FuseDesk case. |

### Case Reply

| Action | Method | Description |
| --- | --- | --- |
| [Reply to Case by Email](actions/reply-to-case-by-email.md) | POST | Sends an email reply for an existing FuseDesk case. |

### Case Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Case Tag](actions/create-case-tag.md) | POST | Creates a new case tag in FuseDesk. |
| [Delete Case Tag](actions/delete-case-tag.md) | DELETE | Archives an existing case tag in FuseDesk. |
| [List Case Tags](actions/list-case-tags.md) | GET | Retrieves case tags from your FuseDesk account. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Close Chat](actions/close-chat.md) | PUT | Closes an existing chat in FuseDesk. |
| [Get Chat](actions/get-chat.md) | GET | Retrieves a chat and its message history from FuseDesk. |
| [List Chats](actions/list-chats.md) | GET | Retrieves active chats from your FuseDesk account. |
| [Update Chat](actions/update-chat.md) | PUT | Updates an existing chat in FuseDesk. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in FuseDesk. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact record from FuseDesk. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in FuseDesk by matching search text. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in FuseDesk. |

### Department

| Action | Method | Description |
| --- | --- | --- |
| [Archive Department](actions/archive-department.md) | DELETE | Archives an existing department in FuseDesk. |
| [Create Department](actions/create-department.md) | POST | Creates a new department in FuseDesk. |
| [Get Department](actions/get-department.md) | GET | Retrieves a department record from FuseDesk. |
| [List Active Departments](actions/list-active-departments.md) | GET | Retrieves active departments from your FuseDesk account. |
| [List All Departments](actions/list-all-departments.md) | GET | Retrieves all departments from your FuseDesk account. |
| [List Archived Departments](actions/list-archived-departments.md) | GET | Retrieves archived departments from your FuseDesk account. |
| [Restore Archived Department](actions/restore-archived-department.md) | PUT | Restores an archived department in FuseDesk. |
| [Update Department](actions/update-department.md) | PUT | Updates an existing department in FuseDesk. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Get Email](actions/get-email.md) | GET | Retrieves an email record from FuseDesk. |
| [Search Emails](actions/search-emails.md) | GET | Finds emails in FuseDesk by matching search filters. |

### Rep

| Action | Method | Description |
| --- | --- | --- |
| [Get Rep](actions/get-rep.md) | GET | Retrieves a rep profile from FuseDesk. |
| [List Reps](actions/list-reps.md) | GET | Retrieves active and disabled reps from FuseDesk. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in FuseDesk. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from FuseDesk. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from your FuseDesk account. |

