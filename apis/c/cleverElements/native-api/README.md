# Clever Elements: Native API Reference

A consolidated summary of Clever Elements's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.cleverelements.com/kb/api/
- **API base URL:** `http://api.sendcockpit.com/server.php`

## Authentication

### SOAP Credentials

Use the Clever Elements SOAP API credentials from the account settings.

### Credentials

- **User ID:** `userId` · required · The Clever Elements SOAP user id.
- **API Key:** `apiKey` · required · The Clever Elements SOAP API key.

[Official authentication documentation](https://docs.cleverelements.com/kb/api/)

## API conventions

Request bodies use XML.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml; charset=utf-8` |

Responses from this API use XML.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add List](actions/add-list.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-11) |
| [Add Subscriber](actions/add-subscriber.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-21) |
| [Add Subscriber DOI](actions/add-subscriber-doi.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-20) |
| [Add Subscriber Field](actions/add-subscriber-field.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-15) |
| [Delete List](actions/delete-list.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-10) |
| [Delete Subscriber](actions/delete-subscriber.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-19) |
| [Delete Subscriber Field](actions/delete-subscriber-field.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-14) |
| [Get List Details](actions/get-list-details.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-12) |
| [Get Subscriber By Email](actions/get-subscriber-by-email.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-6) |
| [Get Subscriber History](actions/get-subscriber-history.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-22) |
| [List Lists](actions/list-lists.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-13) |
| [List Newsletter Receivers](actions/list-newsletter-receivers.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-23) |
| [List Sent Newsletters](actions/list-sent-newsletters.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-24) |
| [List Subscriber Details](actions/list-subscriber-details.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-8) |
| [List Subscriber Fields](actions/list-subscriber-fields.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-16) |
| [List Subscriber Subscriptions](actions/list-subscriber-subscriptions.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-5) |
| [List Subscribers](actions/list-subscribers.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-9) |
| [List Unsubscribed Subscribers](actions/list-unsubscribed-subscribers.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-7) |
| [Unsubscribe Subscriber From All Lists](actions/unsubscribe-subscriber-from-all-lists.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-17) |
| [Unsubscribe Subscriber From List](actions/unsubscribe-subscriber-from-list.md) | `POST /` | [docs](https://docs.cleverelements.com/kb/api/#document-18) |
