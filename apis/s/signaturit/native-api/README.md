# Signaturit: Native API Reference

A consolidated summary of Signaturit's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://docs.signaturit.com/api/latest
- **REST API base URL:** `https://api.sandbox.signaturit.com/v3`
- **REST API base URL:** `https://api.sandbox.signaturit.com`

## Authentication

### Access Token

Use a Signaturit dashboard access token sent as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.signaturit.com/hc/en-us/articles/360000259318-API-Access-get-your-token)

## API conventions

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

- **REST API:** Use `limit` in the query string to set the page size (maximum 100). Use `offset` in the query string as the record offset.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contacts.json` | [docs](https://docs.signaturit.com/api/latest#contacts_post_contact) |
| [Create Subscription](actions/create-subscription.md) | `POST /subscriptions.json` | [docs](https://docs.signaturit.com/api/latest#subscriptions_post_subscription) |
| [Delete Subscription](actions/delete-subscription.md) | `DELETE /subscriptions/:id.json` | [docs](https://docs.signaturit.com/api/latest#subscriptions_delete_subscription) |
| [Get Certified Email](actions/get-certified-email.md) | `GET /emails/:id.json` | [docs](https://docs.signaturit.com/api/latest#emails_get_email) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id.json` | [docs](https://docs.signaturit.com/api/latest#contacts_get_contact) |
| [Get Credits](actions/get-credits.md) | `GET /account/credits.json` | [docs](https://docs.signaturit.com/api/latest#credits_get_credits) |
| [Get Signature](actions/get-signature.md) | `GET /signatures/:id.json` | [docs](https://docs.signaturit.com/api/latest#signatures_get_signature) |
| [List Certified Emails](actions/list-certified-emails.md) | `GET /emails.json` | [docs](https://docs.signaturit.com/api/latest#emails_get_emails) |
| [List Certified SMS](actions/list-certified-sms.md) | `GET /sms.json` | [docs](https://docs.signaturit.com/api/latest#sms_get_sms) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts.json` | [docs](https://docs.signaturit.com/api/latest#contacts_get_contacts) |
| [List Event Hooks](actions/list-event-hooks.md) | `GET /event-hooks` | [docs](https://docs.signaturit.com/api/latest#eventhooks_get) |
| [List Signatures](actions/list-signatures.md) | `GET /signatures.json` | [docs](https://docs.signaturit.com/api/latest#signatures_get_signatures) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /subscriptions.json` | [docs](https://docs.signaturit.com/api/latest#subscriptions_get_subscriptions) |
| [List Templates](actions/list-templates.md) | `GET /templates.json` | [docs](https://docs.signaturit.com/api/latest#templates_get_templates) |
| [List Templates V4](actions/list-templates-v4.md) | `GET https://api.sandbox.signaturit.com/v4/templates` | [docs](https://docs.signaturit.com/api/latest#templates_get_templates_v4) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/:id.json` | [docs](https://docs.signaturit.com/api/latest#contacts_patch_contact) |
| [Update Subscription](actions/update-subscription.md) | `PATCH /subscriptions/:id.json` | [docs](https://docs.signaturit.com/api/latest#subscriptions_patch_subscription) |
