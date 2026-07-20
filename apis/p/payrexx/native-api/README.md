# Payrexx: Native API Reference

A consolidated summary of Payrexx's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://developers.payrexx.com/reference/rest-api
- **API base URL:** `https://api.payrexx.com/v1.14/`

## Authentication

### API Key

Connect Payrexx with an API key from the merchant dashboard and your Payrexx instance name.

### Credentials

- **API Key:** `apiKey` · required
- **Instance:** `instance` · required · Your Payrexx instance name.

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://docs.payrexx.com/merchant/english/account/api-and-plugins)

## API conventions

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `instance` | query | `string` | yes | Your Payrexx instance name. |

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Waiting Transaction](actions/cancel-waiting-transaction.md) | `PATCH Transaction/:id/cancel` | [docs](https://developers.payrexx.com/reference/cancel-a-waiting-transaction) |
| [Capture Transaction](actions/capture-transaction.md) | `POST Transaction/:id/capture` | [docs](https://developers.payrexx.com/reference/capture-a-transaction) |
| [Charge Pre-Authorized Reserved Transaction](actions/charge-pre-authorized-reserved-transaction.md) | `POST Transaction/:id/` | [docs](https://developers.payrexx.com/reference/charge-a-pre-authorized-reserved-transaction) |
| [Create Gateway](actions/create-gateway.md) | `POST Gateway/` | [docs](https://developers.payrexx.com/reference/create-a-gateway) |
| [Create Invoice](actions/create-invoice.md) | `POST Bill/` | [docs](https://developers.payrexx.com/reference/create-an-invoice) |
| [Create Manual Payout](actions/create-manual-payout.md) | `POST Payout/` | [docs](https://developers.payrexx.com/reference/create-manual-payout) |
| [Create Paylink](actions/create-paylink.md) | `POST Invoice/` | [docs](https://developers.payrexx.com/reference/create-a-paylink) |
| [Create QR Code](actions/create-qr-code.md) | `POST QrCode/` | [docs](https://developers.payrexx.com/reference/create-a-qr-code) |
| [Create Subscription](actions/create-subscription.md) | `POST Subscription/` | [docs](https://developers.payrexx.com/reference/create-a-new-subscription) |
| [Delete Gateway](actions/delete-gateway.md) | `DELETE Gateway/:id/` | [docs](https://developers.payrexx.com/reference/delete-a-gateway) |
| [Delete Invoice](actions/delete-invoice.md) | `DELETE Bill/:id/` | [docs](https://developers.payrexx.com/reference/delete-an-invoice) |
| [Delete Paylink](actions/delete-paylink.md) | `DELETE Invoice/:id/` | [docs](https://developers.payrexx.com/reference/remove-a-paylink) |
| [Delete Reserved Transaction](actions/delete-reserved-transaction.md) | `DELETE Transaction/:id/` | [docs](https://developers.payrexx.com/reference/delete-a-reserved-transaction) |
| [Get Design](actions/get-design.md) | `GET Design/:uuid/` | [docs](https://developers.payrexx.com/reference/retrieve-a-design) |
| [Get Gateway](actions/get-gateway.md) | `GET Gateway/:id/` | [docs](https://developers.payrexx.com/reference/retrieve-a-gateway) |
| [Get Invoice](actions/get-invoice.md) | `GET Bill/:id/` | [docs](https://developers.payrexx.com/reference/retrieve-an-invoice) |
| [Get Paylink](actions/get-paylink.md) | `GET Invoice/:id/` | [docs](https://developers.payrexx.com/reference/retrieve-a-paylink) |
| [Get Payment Method](actions/get-payment-method.md) | `GET PaymentMethod/:paymentMethod/` | [docs](https://developers.payrexx.com/reference/get-one-payment-method) |
| [Get Transaction](actions/get-transaction.md) | `GET Transaction/:id/` | [docs](https://developers.payrexx.com/reference/retrieve-a-transaction) |
| [Helper Create Design](actions/helper-create-design.md) | `POST Design/` | [docs](https://developers.payrexx.com/reference/create-a-design) |
| [List Designs](actions/list-designs.md) | `GET Design/` | [docs](https://developers.payrexx.com/reference/retrieve-all-designs) |
| [List Invoices](actions/list-invoices.md) | `GET Bill/` | [docs](https://developers.payrexx.com/reference/list-all-invoices) |
| [List Payment Methods](actions/list-payment-methods.md) | `GET PaymentMethod/` | [docs](https://developers.payrexx.com/reference/get-all-active-payment-methods) |
| [List Payment Providers](actions/list-payment-providers.md) | `GET PaymentProvider/` | [docs](https://developers.payrexx.com/reference/retrieve-all-payment-providers) |
| [List Payouts](actions/list-payouts.md) | `GET Payout/` | [docs](https://developers.payrexx.com/reference/retrieve-payouts) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET Subscription/` | [docs](https://developers.payrexx.com/reference/retrieve-subscriptions) |
| [List Transactions](actions/list-transactions.md) | `GET Transaction/` | [docs](https://developers.payrexx.com/reference/retrieve-transactions) |
| [Pre-Authorize Tokenization](actions/pre-authorize-tokenization.md) | `POST Transaction/:id/preAuthorize` | [docs](https://developers.payrexx.com/reference/pre-authorize-a-tokenization) |
| [Refund Transaction](actions/refund-transaction.md) | `POST Transaction/:id/refund` | [docs](https://developers.payrexx.com/reference/refund-a-transaction) |
| [Send Mail Receipt](actions/send-mail-receipt.md) | `POST Transaction/:id/receipt` | [docs](https://developers.payrexx.com/reference/send-mail-receipt) |
| [Update Invoice](actions/update-invoice.md) | `PATCH Bill/:id/` | [docs](https://developers.payrexx.com/reference/update-an-invoice) |
| [Update Pre-Authorization Tokenization Contact Details](actions/update-pre-authorization-tokenization-contact-details.md) | `PUT Transaction/:id/` | [docs](https://developers.payrexx.com/reference/update-contact-details) |
| [Update Tokenization](actions/update-tokenization.md) | `PATCH Transaction/:id/updateTokenization` | [docs](https://developers.payrexx.com/reference/update-a-tokenization) |
