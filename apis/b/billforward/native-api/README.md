# Billforward: Native API Reference

A consolidated summary of Billforward's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://app.billforward.net/#/api/docs/intro
- **API base URL:** `https://app-sandbox.billforward.net/v1`

## Authentication

### Private Access Token

Use a Billforward private access token for sandbox REST API access.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://billforward.freshdesk.com/support/solutions/articles/77000434962-i-would-like-to-change-the-state-of-a-subscription-how-can-i-do-that-)

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Credit To Account](actions/add-credit-to-account.md) | `POST /accounts/:accountId/credit` | [docs](https://app.billforward.net/#/api/method/accounts) |
| [Create Account](actions/create-account.md) | `POST /accounts` | [docs](https://app.billforward.net/#/api/method/accounts) |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://app.billforward.net/#/api/method/products) |
| [Find Account By Email](actions/find-account-by-email.md) | `GET /accounts/email/:email` | [docs](https://app.billforward.net/#/api/method/accounts) |
| [Get Account](actions/get-account.md) | `GET /accounts/:accountId` | [docs](https://app.billforward.net/#/api/method/accounts) |
| [Get Credit Note](actions/get-credit-note.md) | `GET /credit-notes/:creditNoteId` | [docs](https://app.billforward.net/#/api/method/credit-notes) |
| [Get Product](actions/get-product.md) | `GET /products/:productId` | [docs](https://app.billforward.net/#/api/method/products) |
| [Get Profile](actions/get-profile.md) | `GET /profiles/:profileId` | [docs](https://app.billforward.net/#/api/method/profiles) |
| [List Account Credit Notes](actions/list-account-credit-notes.md) | `GET /accounts/:accountId/credit` | [docs](https://app.billforward.net/#/api/method/accounts) |
| [List Account Invoices](actions/list-account-invoices.md) | `GET /accounts/:accountId/invoices` | [docs](https://app.billforward.net/#/api/method/accounts) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://app.billforward.net/#/api/method/accounts) |
| [List Credit Notes](actions/list-credit-notes.md) | `GET /credit-notes` | [docs](https://app.billforward.net/#/api/method/credit-notes) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://app.billforward.net/#/api/method/invoices) |
| [List Payment Methods](actions/list-payment-methods.md) | `GET /payment-methods` | [docs](https://app.billforward.net/#/api/method/payment-methods) |
| [List Payments](actions/list-payments.md) | `GET /payments` | [docs](https://app.billforward.net/#/api/method/payments) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://app.billforward.net/#/api/method/products) |
| [List Profiles](actions/list-profiles.md) | `GET /profiles` | [docs](https://app.billforward.net/#/api/method/profiles) |
| [List Profiles By Account](actions/list-profiles-by-account.md) | `GET /profiles/account/:accountId` | [docs](https://app.billforward.net/#/api/method/profiles) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /subscriptions` | [docs](https://app.billforward.net/#/api/method/subscriptions) |
| [Update Account](actions/update-account.md) | `PUT /accounts` | [docs](https://app.billforward.net/#/api/method/accounts) |
