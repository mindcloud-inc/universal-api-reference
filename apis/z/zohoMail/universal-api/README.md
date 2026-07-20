# <img src="https://images.mindcloud.co/apps/icons/zoho-mail_1773235889064.png" alt="Zoho Mail logo" width="28" height="28"> Zoho Mail: Universal API

Send, receive, and organize business email conversations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoMail/latest
- **Category:** Communication / Email Communications
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/mail/
- **Vendor API docs:** https://www.zoho.com/mail/help/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Email

| Action | Method | Description |
| --- | --- | --- |
| [List Emails](actions/list-emails.md) | GET | Retrieves email messages from Zoho Mail. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Apply Labels To Emails](actions/apply-labels-to-emails.md) | PUT | Applies labels to emails in Zoho Mail. |
| [Archive Emails](actions/archive-emails.md) | PUT | Archives email messages in Zoho Mail. |
| [Delete Email](actions/delete-email.md) | DELETE | Deletes an email from Zoho Mail. |
| [Download Attachment](actions/download-attachment.md) | GET | Retrieves attachment content from Zoho Mail. |
| [Flag Emails](actions/flag-emails.md) | PUT | Flags email messages in Zoho Mail. |
| [Get Attachment Info](actions/get-attachment-info.md) | GET | Retrieves attachment info from Zoho Mail. |
| [Get Email Content](actions/get-email-content.md) | GET | Retrieves email content from Zoho Mail. |
| [Get Email Metadata](actions/get-email-metadata.md) | GET | Retrieves email metadata from Zoho Mail. |
| [Mark Emails Read](actions/mark-emails-read.md) | PUT | Marks emails as read in Zoho Mail. |
| [Mark Emails Unread](actions/mark-emails-unread.md) | PUT | Marks emails as unread in Zoho Mail. |
| [Move Emails](actions/move-emails.md) | PUT | Moves emails to a folder in Zoho Mail. |
| [Reply To Email](actions/reply-to-email.md) | POST | Replies to an email in Zoho Mail. |
| [Save Draft](actions/save-draft.md) | POST | Creates a draft email in Zoho Mail. |
| [Search Emails](actions/search-emails.md) | GET | Finds emails in Zoho Mail by search parameters. |
| [Send Email](actions/send-email.md) | POST | Sends an email through Zoho Mail. |

### Mail Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET | Retrieves account details from Zoho Mail. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves all mail accounts from Zoho Mail. |

### Mail Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Zoho Mail. |
| [Get Folder](actions/get-folder.md) | GET | Retrieves a folder from Zoho Mail. |
| [List Folders](actions/list-folders.md) | GET | Retrieves all folders from Zoho Mail. |

### Mail Label

| Action | Method | Description |
| --- | --- | --- |
| [Create Label](actions/create-label.md) | POST | Creates a new label in Zoho Mail. |
| [List Labels](actions/list-labels.md) | GET | Retrieves all labels from Zoho Mail. |

