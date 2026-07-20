# AvoSMS: Native API Reference

A consolidated summary of AvoSMS's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://www.avosms.com/en/api/documentation
- **API base URL:** `https://api.avosms.com`

## Authentication

### API Key

Use your AvoSMS account email and API key.

### Credentials

- **API Key:** `apiKey` · required
- **Account ID:** `accountId` · required · Your AvoSMS account ID (email address).

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.avosms.com/en/api/documentation)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact](actions/add-contact.md) | `POST /v1/contact/add` | [docs](https://www.avosms.com/en/api/documentation/contact/add) |
| [Create Contact List](actions/create-contact-list.md) | `POST /v1/contact/list/create` | [docs](https://www.avosms.com/en/api/documentation/contact/list/create) |
| [Create Sender](actions/create-sender.md) | `POST /v1/sender/create` | [docs](https://www.avosms.com/en/api/documentation/sender/create) |
| [Create SMS Template](actions/create-sms-template.md) | `POST /v1/model/sms/create` | [docs](https://www.avosms.com/en/api/documentation/model/sms/create) |
| [Delete Contact](actions/delete-contact.md) | `POST /v1/contact/delete` | [docs](https://www.avosms.com/en/api/documentation/contact/delete) |
| [Delete Contact List](actions/delete-contact-list.md) | `POST /v1/contact/list/delete` | [docs](https://www.avosms.com/en/api/documentation/contact/list/delete) |
| [Delete Sender](actions/delete-sender.md) | `POST /v1/sender/delete` | [docs](https://www.avosms.com/en/api/documentation/sender/delete) |
| [Delete SMS Template](actions/delete-sms-template.md) | `POST /v1/model/sms/delete` | [docs](https://www.avosms.com/en/api/documentation/model/sms/delete) |
| [Get Account Balance](actions/get-account-balance.md) | `POST /v1/account/balance` | [docs](https://www.avosms.com/en/api/documentation/compte/balance) |
| [Get Contact List](actions/get-contact-list.md) | `POST /v1/contact/list/information` | [docs](https://www.avosms.com/en/api/documentation/contact/list/information) |
| [Get SMS Template](actions/get-sms-template.md) | `POST /v1/model/sms/information` | [docs](https://www.avosms.com/en/api/documentation/model/sms/information) |
| [List Available Destinations](actions/list-available-destinations.md) | `POST /v1/list/country` | [docs](https://www.avosms.com/en/api/documentation/country/available) |
| [List Contact Lists](actions/list-contact-lists.md) | `POST /v1/contact/list` | [docs](https://www.avosms.com/en/api/documentation/contact/list) |
| [List Senders](actions/list-senders.md) | `POST /v1/sender/list` | [docs](https://www.avosms.com/en/api/documentation/sender/list) |
| [List SMS Responses](actions/list-sms-responses.md) | `POST /v1/response/list` | [docs](https://www.avosms.com/en/api/documentation/response-sms/list) |
| [List SMS Templates](actions/list-sms-templates.md) | `POST /v1/model/sms/list` | [docs](https://www.avosms.com/en/api/documentation/model/sms/list) |
| [Rename Contact List](actions/rename-contact-list.md) | `POST /v1/contact/list/rename` | [docs](https://www.avosms.com/en/api/documentation/contact/list/rename) |
| [Send SMS](actions/send-sms.md) | `POST /v1/sms/send` | [docs](https://www.avosms.com/en/api/documentation/sms/send) |
| [Update Contact](actions/update-contact.md) | `POST /v1/contact/update` | [docs](https://www.avosms.com/en/api/documentation/contact/update) |
| [Update SMS Template](actions/update-sms-template.md) | `POST /v1/model/sms/update` | [docs](https://www.avosms.com/en/api/documentation/model/sms/update) |
