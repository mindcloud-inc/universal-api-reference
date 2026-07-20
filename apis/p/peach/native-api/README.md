# Peach: Native API Reference

A consolidated summary of Peach's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://peach-organization.gitbook.io/peach/api-reference
- **API base URL:** `https://api.peach-in.com/v4`

## Authentication

### API Key

Use a Peach API key generated from Peach Developer Tools.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://peach-organization.gitbook.io/peach/api-reference/authentication)

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | `PUT /payment/:paymentId` | [docs](https://peach-organization.gitbook.io/peach/api-reference/payments/update-payment) |
| [Change Subscription Charge Day](actions/change-subscription-charge-day.md) | `PUT /payment/:paymentId` | [docs](https://peach-organization.gitbook.io/peach/api-reference/payments/update-payment) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://peach-organization.gitbook.io/peach/api-reference/contacts/create-contact) |
| [Create Note](actions/create-note.md) | `POST /notes` | [docs](https://peach-organization.gitbook.io/peach/api-reference/interactions/create-note) |
| [Create One-Time Payment](actions/create-one-time-payment.md) | `POST /payments` | [docs](https://peach-organization.gitbook.io/peach/api-reference/payments/create-payment) |
| [Create Subscription Payment](actions/create-subscription-payment.md) | `POST /payments` | [docs](https://peach-organization.gitbook.io/peach/api-reference/payments/create-payment) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /deleteContact` | [docs](https://peach-organization.gitbook.io/peach/api-reference/contacts/delete-contact) |
| [Freeze Subscription](actions/freeze-subscription.md) | `PUT /payment/:paymentId` | [docs](https://peach-organization.gitbook.io/peach/api-reference/payments/update-payment) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/:campaignId` | [docs](https://peach-organization.gitbook.io/peach/api-reference/campaigns/get-campiagn) |
| [Get Campaign Stats](actions/get-campaign-stats.md) | `GET /campaigns/stats/:accountId/:campaignId` | [docs](https://peach-organization.gitbook.io/peach/api-reference/campaigns/get-campaign-stats) |
| [Get Contact By Email](actions/get-contact-by-email.md) | `POST /getContact` | [docs](https://peach-organization.gitbook.io/peach/api-reference/contacts/get-contact) |
| [Get Contact By ID](actions/get-contact-by-id.md) | `POST /getContact` | [docs](https://peach-organization.gitbook.io/peach/api-reference/contacts/get-contact) |
| [Get Contact By Phone](actions/get-contact-by-phone.md) | `POST /getContact` | [docs](https://peach-organization.gitbook.io/peach/api-reference/contacts/get-contact) |
| [Get Contact By Tz](actions/get-contact-by-tz.md) | `POST /getContact` | [docs](https://peach-organization.gitbook.io/peach/api-reference/contacts/get-contact) |
| [List Transactions](actions/list-transactions.md) | `POST /transactions/search` | [docs](https://peach-organization.gitbook.io/peach/api-reference/transactions/get-transactions) |
| [List Transactions By Campaign](actions/list-transactions-by-campaign.md) | `POST /transactions/search` | [docs](https://peach-organization.gitbook.io/peach/api-reference/transactions/get-transactions) |
| [Update Contact](actions/update-contact.md) | `PUT /updateContact/:contactId` | [docs](https://peach-organization.gitbook.io/peach/api-reference/contacts/update-contact) |
| [Update Payment Field](actions/update-payment-field.md) | `PUT /payment/:paymentId` | [docs](https://peach-organization.gitbook.io/peach/api-reference/payments/update-payment) |
| [Update Subscription Additional Sum](actions/update-subscription-additional-sum.md) | `PUT /payment/:paymentId` | [docs](https://peach-organization.gitbook.io/peach/api-reference/payments/update-payment) |
| [Update Subscription Cycles](actions/update-subscription-cycles.md) | `PUT /payment/:paymentId` | [docs](https://peach-organization.gitbook.io/peach/api-reference/payments/update-payment) |
