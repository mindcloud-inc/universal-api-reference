# <img src="https://images.mindcloud.co/apps/icons/outlook-icon_1777571198504.png" alt="Outlook logo" width="28" height="28"> Outlook: Universal API

Read Outlook mailbox messages through Microsoft Graph using delegated OAuth access.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/outlook/latest
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://outlook.live.com
- **Vendor API docs:** https://learn.microsoft.com/en-us/graph/api/resources/message

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Messages](actions/list-messages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outlook/latest/actions/list-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [List Message Attachments](actions/list-message-attachments.md) | GET | Retrieves attachments for an Outlook email. |

### Mail Folder

| Action | Method | Description |
| --- | --- | --- |
| [Get Mail Folder](actions/get-mail-folder.md) | GET | Retrieves an Outlook mail folder by folder ID. |
| [List Mail Folders](actions/list-mail-folders.md) | GET | Retrieves mail folders from an Outlook mailbox. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Draft Message](actions/create-draft-message.md) | POST | Creates a draft email in Outlook. |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes an existing email from Outlook. |
| [Get Message](actions/get-message.md) | GET | Retrieves an email from Outlook by message ID. |
| [List Folder Messages](actions/list-folder-messages.md) | GET | Retrieves emails from a specific Outlook mail folder. |
| [List Messages](actions/list-messages.md) | GET | Retrieves email messages from an Outlook mailbox. |
| [Send Draft Message](actions/send-draft-message.md) | POST | Sends an existing draft email from Outlook. |
| [Send Mail](actions/send-mail.md) | POST | Sends a new email from Outlook. |
| [Update Message](actions/update-message.md) | PUT | Updates an existing Outlook email, with some fields draft-only. |

