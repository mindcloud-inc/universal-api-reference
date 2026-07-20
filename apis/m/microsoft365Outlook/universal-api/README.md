# <img src="https://images.mindcloud.co/apps/icons/microsoft-icon_1776116500237.png" alt="Microsoft 365 Outlook logo" width="28" height="28"> Microsoft 365 Outlook: Universal API

Access Microsoft 365 Outlook mail through Microsoft Graph, including messages, folders, attachments, replies, forwarding, and sending mail for the signed-in user.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/microsoft365Outlook/latest
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.microsoft.com/microsoft-365/outlook/email-and-calendar-software-microsoft-outlook
- **Vendor API docs:** https://learn.microsoft.com/en-us/graph/use-the-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Inbox Messages](actions/list-inbox-messages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/list-inbox-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Add File Attachment to Message](actions/add-file-attachment-to-message.md) | POST | Adds a file attachment to a message in Microsoft 365 Outlook. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [List Child Mail Folders](actions/list-child-mail-folders.md) | GET | Retrieves child mail folders from Microsoft 365 Outlook. |
| [List Mail Folders](actions/list-mail-folders.md) | GET | Retrieves mail folders from Microsoft 365 Outlook. |

### Message Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Get Message Attachment](actions/get-message-attachment.md) | GET | Retrieves an attachment from Microsoft 365 Outlook. |
| [List Message Attachments](actions/list-message-attachments.md) | GET | Retrieves attachments for a message from Microsoft 365 Outlook. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Draft Message](actions/create-draft-message.md) | POST | Creates a draft message in Microsoft 365 Outlook. |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes a message from Microsoft 365 Outlook. |
| [Forward Message](actions/forward-message.md) | POST | Forwards a message from Microsoft 365 Outlook. |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from Microsoft 365 Outlook. |
| [List Inbox Messages](actions/list-inbox-messages.md) | GET | Retrieves inbox messages from Microsoft 365 Outlook. |
| [List Messages in Folder](actions/list-messages-in-folder.md) | GET | Retrieves messages from a mail folder in Microsoft 365 Outlook. |
| [Move Message](actions/move-message.md) | PUT | Moves a message to another mail folder in Microsoft 365 Outlook. |
| [Reply All to Message](actions/reply-all-to-message.md) | POST | Replies to all recipients of a message in Microsoft 365 Outlook. |
| [Reply to Message](actions/reply-to-message.md) | POST | Replies to a message in Microsoft 365 Outlook. |
| [Send Draft Message](actions/send-draft-message.md) | PUT | Sends a draft message in Microsoft 365 Outlook. |
| [Send Mail](actions/send-mail.md) | POST | Sends a new message from Microsoft 365 Outlook. |
| [Update Draft Message](actions/update-draft-message.md) | PUT | Updates an existing draft message in Microsoft 365 Outlook. |

