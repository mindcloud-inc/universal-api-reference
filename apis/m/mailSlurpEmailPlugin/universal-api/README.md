# <img src="https://images.mindcloud.co/apps/icons/mailslurp-icon_1775680236476.png" alt="MailSlurp Email Plugin logo" width="28" height="28"> MailSlurp Email Plugin: Universal API

MailSlurp email and inbox automation for creating inboxes, sending and inspecting emails, managing contacts, attachments, templates, webhooks, and wait-for email workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mailSlurpEmailPlugin/latest
- **Category:** Communication / Email Communications
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mailslurp.com
- **Vendor API docs:** https://docs.mailslurp.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Inboxes](actions/list-inboxes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/list-inboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [List Attachments](actions/list-attachments.md) | GET | Retrieves attachments from your MailSlurp account. |
| [Upload Attachment](actions/upload-attachment.md) | POST | Uploads an attachment to your MailSlurp account. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in MailSlurp. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from your MailSlurp account. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Check If Email Can Send](actions/check-if-email-can-send.md) | GET | Checks whether MailSlurp can send an email. |
| [Delete Email](actions/delete-email.md) | DELETE | Deletes an existing email from MailSlurp. |
| [Forward Email](actions/forward-email.md) | POST | Forwards an existing email from MailSlurp. |
| [Get Email](actions/get-email.md) | GET | Retrieves a hydrated email from MailSlurp. |
| [Get Email Codes](actions/get-email-codes.md) | GET | Extracts verification codes from an email in MailSlurp. |
| [Get Email Content Match](actions/get-email-content-match.md) | GET | Finds regex matches in a MailSlurp email body. |
| [List Emails](actions/list-emails.md) | GET | Retrieves emails across all MailSlurp inboxes. |
| [Mark Email Read State](actions/mark-email-read-state.md) | PUT | Updates an email's read state in MailSlurp. |
| [Reply To Email](actions/reply-to-email.md) | POST | Replies to an email in MailSlurp. |
| [Search Emails](actions/search-emails.md) | GET | Finds emails in MailSlurp by search criteria. |
| [Send Email And Confirm](actions/send-email-and-confirm.md) | POST | Sends an email from MailSlurp and returns the confirmation. |
| [Send Email From Inbox](actions/send-email-from-inbox.md) | POST | Sends an email from an inbox in MailSlurp. |
| [Send Email With Queue](actions/send-email-with-queue.md) | POST | Sends an email from MailSlurp using the sending queue. |
| [Send Test Email](actions/send-test-email.md) | POST | Sends a test email to an inbox in MailSlurp. |
| [Wait For Latest Email](actions/wait-for-latest-email.md) | GET | Retrieves the latest email from MailSlurp, waiting if needed. |
| [Wait For Matching Emails](actions/wait-for-matching-emails.md) | GET | Waits for MailSlurp emails that match the given filters. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in MailSlurp. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from your MailSlurp account. |

### Inbox

| Action | Method | Description |
| --- | --- | --- |
| [Create Inbox With Defaults](actions/create-inbox-with-defaults.md) | POST | Creates a new inbox in MailSlurp with default settings. |
| [Create Inbox With Options](actions/create-inbox-with-options.md) | POST | Creates a new inbox in MailSlurp with custom options. |
| [Delete Inbox](actions/delete-inbox.md) | DELETE | Deletes an existing inbox from MailSlurp. |
| [Get Inbox](actions/get-inbox.md) | GET | Retrieves an inbox and its details from MailSlurp. |
| [List Inboxes](actions/list-inboxes.md) | GET | Retrieves inboxes and email addresses from MailSlurp. |
| [Search Inboxes](actions/search-inboxes.md) | GET | Finds inboxes in MailSlurp by search criteria. |
| [Update Inbox](actions/update-inbox.md) | PUT | Updates an existing inbox in MailSlurp. |

### Scheduled Job

| Action | Method | Description |
| --- | --- | --- |
| [Send Email With Schedule](actions/send-email-with-schedule.md) | POST | Schedules an email to send from MailSlurp. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in MailSlurp. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from your MailSlurp account. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from your MailSlurp account. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in MailSlurp. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from your MailSlurp account. |

