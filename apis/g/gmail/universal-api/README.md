# <img src="https://images.mindcloud.co/apps/icons/gmail-default-1_1779719609775.png" alt="Google Mail logo" width="28" height="28"> Google Mail: Universal API

Send email, organize inboxes, search messages, and collaborate faster.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gmail/latest
- **Category:** Communication / Team Messaging
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mail.google.com/
- **Vendor API docs:** https://developers.google.com/workspace/gmail/api/reference/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Labels](actions/list-labels.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/list-labels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Authenticate

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET | Retrieves the current user's Gmail profile. |

### Email Label

| Action | Method | Description |
| --- | --- | --- |
| [Create Label](actions/create-label.md) | POST | Creates a Gmail label. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Batch Modify Emails](actions/batch-modify-emails.md) | PUT | Updates labels on multiple Gmail messages. |
| [Create Draft](actions/create-draft.md) | POST | Creates a Gmail draft. |
| [Delete Draft](actions/delete-draft.md) | DELETE | Deletes a Gmail draft permanently. |
| [Get Draft](actions/get-draft.md) | GET | Retrieves a Gmail draft. |
| [Get Email](actions/get-email.md) | GET | Retrieves a Gmail message. |
| [Get Email Attachment](actions/get-email-attachment.md) | GET | Retrieves a Gmail message attachment. |
| [Get Email Signature](actions/get-email-signature.md) | GET | Retrieves a Gmail signature. |
| [Get Filter](actions/get-filter.md) | GET | Retrieves a filter from Gmail settings. |
| [Get Thread](actions/get-thread.md) | GET | Retrieves a Gmail thread. |
| [Get Vacation Settings](actions/get-vacation-settings.md) | GET | Retrieves vacation responder settings from Gmail. |
| [Import Email](actions/import-email.md) | POST | Imports a message into Gmail. |
| [Insert Email](actions/insert-email.md) | POST | Inserts a message into Gmail. |
| [List Drafts](actions/list-drafts.md) | GET | Retrieves drafts from a Gmail mailbox. |
| [List Emails](actions/list-emails.md) | GET | Retrieves messages from a Gmail mailbox. |
| [List Filters](actions/list-filters.md) | GET | Retrieves filters from Gmail settings. |
| [List Threads](actions/list-threads.md) | GET | Retrieves threads from a Gmail mailbox. |
| [Modify Email Labels](actions/modify-email-labels.md) | PUT | Updates labels on a Gmail message. |
| [Modify Thread Labels](actions/modify-thread-labels.md) | PUT | Updates labels on a Gmail thread. |
| [Send Draft](actions/send-draft.md) | POST | Sends a Gmail draft. |
| [Send Email](actions/send-email.md) | POST | Sends a Gmail message. |
| [Start Mailbox Watch (Action)](actions/start-mailbox-watch-action.md) | POST | Sets up or updates a Gmail mailbox watch. |
| [Stop Mailbox Watch](actions/stop-mailbox-watch.md) | PUT | Stops Gmail mailbox push notifications. |
| [Trash Email](actions/trash-email.md) | PUT | Moves a Gmail message to trash. |
| [Trash Thread](actions/trash-thread.md) | PUT | Moves a Gmail thread to trash. |
| [Untrash Email](actions/untrash-email.md) | PUT | Removes a Gmail message from trash. |
| [Untrash Thread](actions/untrash-thread.md) | PUT | Removes a Gmail thread from trash. |
| [Update Draft](actions/update-draft.md) | PUT | Updates a Gmail draft. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Delete Label](actions/delete-label.md) | DELETE | Deletes a Gmail label. |
| [Get Label](actions/get-label.md) | GET | Retrieves a Gmail label. |
| [List Labels](actions/list-labels.md) | GET | Retrieves labels from a Gmail mailbox. |
| [Patch Label](actions/patch-label.md) | PUT | Updates a Gmail label. |
| [Update Label](actions/update-label.md) | PUT | Updates a Gmail label. |

