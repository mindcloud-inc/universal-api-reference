# SendMe: Native API Reference

A consolidated summary of SendMe's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://docs.sendme123.com/en/api/
- **API base URL:** `https://app.sendme123.com`

## Authentication

### API Key Header

Authenticate requests with the SendMe `api-key` header.

### Credentials

- **API Key:** `apiKey` · required · SendMe API key value from Settings > General > API Keys.

Send these headers with each API request:

```http
api-key: <apiKey>
```

[Official authentication documentation](https://docs.sendme123.com/en/api/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /api/contacts` | [docs](https://docs.sendme123.com/en/api/contacts/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /api/contacts/:id` | [docs](https://docs.sendme123.com/en/api/contacts/delete/) |
| [Get Contact](actions/get-contact.md) | `GET /api/contacts/:id` | [docs](https://docs.sendme123.com/en/api/contacts/get-by-id/) |
| [List Contacts](actions/list-contacts.md) | `GET /api/contacts` | [docs](https://docs.sendme123.com/en/api/contacts/) |
| [List Messages](actions/list-messages.md) | `GET /api/messages` | [docs](https://docs.sendme123.com/en/api/messages/list/) |
| [Send Email by Tags](actions/send-email-by-tags.md) | `POST /api/messages/email/tags` | [docs](https://docs.sendme123.com/en/api/messages/email-tags/) |
| [Send Email to All](actions/send-email-to-all.md) | `POST /api/messages/email/all` | [docs](https://docs.sendme123.com/en/api/messages/email-all/) |
| [Send Email to Contacts](actions/send-email-to-contacts.md) | `POST /api/messages/email/contacts` | [docs](https://docs.sendme123.com/en/api/messages/email-contacts/) |
| [Send SMS by Tags](actions/send-sms-by-tags.md) | `POST /api/messages/sms/tags` | [docs](https://docs.sendme123.com/en/api/messages/sms-tags/) |
| [Send SMS to All](actions/send-sms-to-all.md) | `POST /api/messages/sms/all` | [docs](https://docs.sendme123.com/en/api/messages/sms-all/) |
| [Send SMS to Contacts](actions/send-sms-to-contacts.md) | `POST /api/messages/sms/contacts` | [docs](https://docs.sendme123.com/en/api/messages/sms-contacts/) |
| [Update Contact](actions/update-contact.md) | `PATCH /api/contacts/:id` | [docs](https://docs.sendme123.com/en/api/contacts/update/) |
