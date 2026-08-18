# <img src="https://images.mindcloud.co/apps/icons/microsoft-exchange-2019-present_1776206436040.png" alt="Microsoft Exchange logo" width="28" height="28"> Microsoft Exchange: Universal API

Connect to Microsoft Exchange mail through Microsoft Graph.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/microsoftExchange/latest
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://learn.microsoft.com/en-us/graph/api/resources/mail-api-overview?view=graph-rest-1.0

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Authorize Application](actions/authorize-application.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/authorize-application?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Authorize Application](actions/authorize-application.md) | GET |  |

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Add File Attachment to Message](actions/add-file-attachment-to-message.md) | POST | Creates a file attachment on a message in Microsoft Exchange. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [List Child Mail Folders](actions/list-child-mail-folders.md) | GET | Retrieves child mail folders from Microsoft Exchange. |
| [List Mail Folders](actions/list-mail-folders.md) | GET | Retrieves mail folders from Microsoft Exchange. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Get User Folder Name](actions/get-user-folder-name.md) | GET | Finds messages in a user's mailbox. |
| [List User Folders](actions/list-user-folders.md) | GET | Finds messages in a user's mailbox. |
| [List User Messages in Folder](actions/list-user-messages-in-folder.md) | GET | Finds messages in a user's mail folder in Microsoft Exchange. |
| [List User Messages in Mailbox](actions/list-user-messages-in-mailbox.md) | GET | Finds messages in a user's mailbox. |

### Message Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Get Message Attachment](actions/get-message-attachment.md) | GET | Retrieves a message attachment from Microsoft Exchange. |
| [List Message Attachments](actions/list-message-attachments.md) | GET | Retrieves attachments for a message from Microsoft Exchange. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Draft Message](actions/create-draft-message.md) | POST | Creates a draft message in Microsoft Exchange. |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes a message from Microsoft Exchange. |
| [Forward Message](actions/forward-message.md) | POST | Forwards a message from Microsoft Exchange. |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from Microsoft Exchange. |
| [List Inbox Messages](actions/list-inbox-messages.md) | GET | Finds inbox messages in Microsoft Exchange by newest first. |
| [List Messages in Folder](actions/list-messages-in-folder.md) | GET | Finds messages in a mail folder in Microsoft Exchange. |
| [Move Message](actions/move-message.md) | PUT | Moves a message to another folder in Microsoft Exchange. |
| [Reply All to Message](actions/reply-all-to-message.md) | POST | Replies to all recipients of a message in Microsoft Exchange. |
| [Reply to Message](actions/reply-to-message.md) | POST | Replies to a message in Microsoft Exchange. |
| [Send Draft Message](actions/send-draft-message.md) | PUT | Sends a draft message in Microsoft Exchange. |
| [Send Mail](actions/send-mail.md) | POST | Sends an email from Microsoft Exchange. |
| [Update Draft Message](actions/update-draft-message.md) | PUT | Updates an existing draft message in Microsoft Exchange. |

