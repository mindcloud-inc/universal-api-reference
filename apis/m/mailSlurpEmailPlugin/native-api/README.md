# MailSlurp Email Plugin: Native API Reference

A consolidated summary of MailSlurp Email Plugin's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://docs.mailslurp.com/api/
- **OpenAPI specification:** https://api.mailslurp.com/v2/api-docs/
- **API base URL:** `https://api.mailslurp.com`

## Authentication

### MailSlurp API Key

Use your MailSlurp API key. MailSlurp REST requests require the key in the shared x-api-key header.

### Credentials

- **API Key:** `apiKey` · required · Your MailSlurp API key. MailSlurp sends this value as the shared x-api-key header on every request.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.mailslurp.com/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check If Email Can Send](actions/check-if-email-can-send.md) | `POST /emails/can-send` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/EmailController/canSend) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/ContactController/createContact) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/GroupController/createGroup) |
| [Create Inbox With Defaults](actions/create-inbox-with-defaults.md) | `POST /inboxes/withDefaults` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/InboxController/createInboxWithDefaults) |
| [Create Inbox With Options](actions/create-inbox-with-options.md) | `POST /inboxes/withOptions` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/InboxController/createInboxWithOptions) |
| [Create Template](actions/create-template.md) | `POST /templates` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/TemplateController/createTemplate) |
| [Create Webhook](actions/create-webhook.md) | `POST /inboxes/:inboxId/webhooks` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/WebhookController/createWebhook) |
| [Delete Email](actions/delete-email.md) | `DELETE /emails/:emailId` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/EmailController/deleteEmail) |
| [Delete Inbox](actions/delete-inbox.md) | `DELETE /inboxes/:inboxId` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/InboxController/deleteInbox) |
| [Forward Email](actions/forward-email.md) | `POST /emails/:emailId/forward` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/EmailController/forwardEmail) |
| [Get Email](actions/get-email.md) | `GET /emails/:emailId` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/EmailController/getEmail) |
| [Get Email Codes](actions/get-email-codes.md) | `POST /emails/:emailId/codes` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/EmailController/getEmailCodes) |
| [Get Email Content Match](actions/get-email-content-match.md) | `POST /emails/:emailId/contentMatch` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/EmailController/getEmailContentMatch) |
| [Get Inbox](actions/get-inbox.md) | `GET /inboxes/:inboxId` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/InboxController/getInbox) |
| [Get Template](actions/get-template.md) | `GET /templates/:templateId` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/TemplateController/getTemplate) |
| [List Attachments](actions/list-attachments.md) | `GET /attachments` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/AttachmentController/getAttachments) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/ContactController/getContacts) |
| [List Emails](actions/list-emails.md) | `GET /emails` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/EmailController/getEmailsPaginated) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/GroupController/getGroups) |
| [List Inboxes](actions/list-inboxes.md) | `GET /inboxes` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/InboxController/getInboxes) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/TemplateController/getTemplates) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks/paginated` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/WebhookController/getAllWebhooks) |
| [Mark Email Read State](actions/mark-email-read-state.md) | `PATCH /emails/:emailId/read` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/EmailController/markAsRead) |
| [Reply To Email](actions/reply-to-email.md) | `PUT /emails/:emailId` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/EmailController/replyToEmail) |
| [Search Emails](actions/search-emails.md) | `POST /emails/search` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/EmailController/searchEmails) |
| [Search Inboxes](actions/search-inboxes.md) | `POST /inboxes/search` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/InboxController/searchInboxes) |
| [Send Email And Confirm](actions/send-email-and-confirm.md) | `POST /inboxes/:inboxId/confirm` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/InboxController/sendEmailAndConfirm) |
| [Send Email From Inbox](actions/send-email-from-inbox.md) | `POST /inboxes/:inboxId` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/InboxController/sendEmail) |
| [Send Email With Queue](actions/send-email-with-queue.md) | `POST /inboxes/:inboxId/with-queue` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/InboxController/sendEmailWithQueue) |
| [Send Email With Schedule](actions/send-email-with-schedule.md) | `POST /inboxes/:inboxId/with-schedule` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/InboxController/sendWithSchedule) |
| [Send Test Email](actions/send-test-email.md) | `POST /inboxes/:inboxId/send-test-email` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/InboxController/sendTestEmail) |
| [Update Inbox](actions/update-inbox.md) | `PATCH /inboxes/:inboxId` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/InboxController/updateInbox) |
| [Upload Attachment](actions/upload-attachment.md) | `POST /attachments` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/AttachmentController/uploadAttachment) |
| [Wait For Latest Email](actions/wait-for-latest-email.md) | `GET /waitForLatestEmail` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/WaitForController/waitForLatestEmail) |
| [Wait For Matching Emails](actions/wait-for-matching-emails.md) | `POST /waitForMatchingEmails` | [docs](https://api.mailslurp.com/swagger-ui/index.html#/WaitForController/waitForMatchingEmails) |
