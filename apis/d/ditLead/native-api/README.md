# DitLead: Native API Reference

A consolidated summary of DitLead's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://ditlead.com/developer/api
- **OpenAPI specification:** https://api.ditlead.com/v1/docs.json
- **API base URL:** `https://api.ditlead.com`

## Authentication

### API Key

Use a DitLead API key from Settings > API keys. MindCloud sends it as an Authorization bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://ditlead.com/developer/api)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact To List](actions/add-contact-to-list.md) | `POST /v1/contact/{contactId}/add-to-list` | [docs](https://ditlead.com/developer/api) |
| [Check Mailbox DKIM](actions/check-mailbox-dkim.md) | `POST /v1/mailbox/check-dkim` | [docs](https://ditlead.com/developer/api) |
| [Check Mailbox DMARC](actions/check-mailbox-dmarc.md) | `POST /v1/mailbox/check-dmarc` | [docs](https://ditlead.com/developer/api) |
| [Check Mailbox SPF](actions/check-mailbox-spf.md) | `POST /v1/mailbox/check-spf` | [docs](https://ditlead.com/developer/api) |
| [Create Contact](actions/create-contact.md) | `POST /v1/contact` | [docs](https://ditlead.com/developer/api) |
| [Create List](actions/create-list.md) | `POST /v1/list` | [docs](https://ditlead.com/developer/api) |
| [Create Mailbox](actions/create-mailbox.md) | `POST /v1/mailbox` | [docs](https://ditlead.com/developer/api) |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /v1/webhook` | [docs](https://ditlead.com/developer/api) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /v1/contact/{contactId}` | [docs](https://ditlead.com/developer/api) |
| [Delete List](actions/delete-list.md) | `DELETE /v1/list/{listId}` | [docs](https://ditlead.com/developer/api) |
| [Delete Mailbox](actions/delete-mailbox.md) | `DELETE /v1/mailbox` | [docs](https://ditlead.com/developer/api) |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | `DELETE /v1/webhook` | [docs](https://ditlead.com/developer/api) |
| [Get Campaigns](actions/get-campaigns.md) | `GET /v1/campaign` | [docs](https://ditlead.com/developer/api) |
| [Get Contact](actions/get-contact.md) | `GET /v1/contact/{contactId}` | [docs](https://ditlead.com/developer/api) |
| [Get Contacts](actions/get-contacts.md) | `GET /v1/contact` | [docs](https://ditlead.com/developer/api) |
| [Get List](actions/get-list.md) | `GET /v1/list/{listId}` | [docs](https://ditlead.com/developer/api) |
| [Get Lists](actions/get-lists.md) | `GET /v1/list` | [docs](https://ditlead.com/developer/api) |
| [Get Mailbox](actions/get-mailbox.md) | `GET /v1/mailbox/{mailboxId}` | [docs](https://ditlead.com/developer/api) |
| [Get Mailbox Insight](actions/get-mailbox-insight.md) | `GET /v1/mailbox/insight/{mailboxId}` | [docs](https://ditlead.com/developer/api) |
| [Get Mailboxes](actions/get-mailboxes.md) | `GET /v1/mailbox` | [docs](https://ditlead.com/developer/api) |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | `GET /v1/webhook` | [docs](https://ditlead.com/developer/api) |
| [Reconnect Mailbox](actions/reconnect-mailbox.md) | `POST /v1/mailbox/reconnect` | [docs](https://ditlead.com/developer/api) |
| [Remove Contact From List](actions/remove-contact-from-list.md) | `POST /v1/contact/{contactId}/remove-from-list` | [docs](https://ditlead.com/developer/api) |
| [Send Warming Emails](actions/send-warming-emails.md) | `POST /v1/mailbox/warming/send` | [docs](https://ditlead.com/developer/api) |
| [Set Mailbox Warming](actions/set-mailbox-warming.md) | `POST /v1/mailbox/warming` | [docs](https://ditlead.com/developer/api) |
| [Update Contact](actions/update-contact.md) | `PUT /v1/contact/{contactId}` | [docs](https://ditlead.com/developer/api) |
| [Update Mailbox](actions/update-mailbox.md) | `PUT /v1/mailbox/{mailboxId}` | [docs](https://ditlead.com/developer/api) |
| [Validate API Key](actions/validate-api-key.md) | `POST /v1/apikey/validate` | [docs](https://ditlead.com/developer/api) |
| [Validate Mailbox SMTP IMAP](actions/validate-mailbox-smtp-imap.md) | `POST /v1/mailbox/validate` | [docs](https://ditlead.com/developer/api) |
| [Verify Email](actions/verify-email.md) | `POST /v1/verify-email` | [docs](https://ditlead.com/developer/api) |
