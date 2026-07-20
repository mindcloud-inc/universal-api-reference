# Trolley: Native API Reference

A consolidated summary of Trolley's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://developers.trolley.com/api/
- **API base URL:** `https://api.trolley.com`

## Authentication

### API Credentials

Use your Trolley API access key as the username and your secret key as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developers.trolley.com/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | `POST /v1/invoices/create` | [docs](https://developers.trolley.com/api/#create-an-invoice) |
| [Create Invoice Lines](actions/create-invoice-lines.md) | `POST /v1/invoices/create-lines` | [docs](https://developers.trolley.com/api/#create-an-invoice-line) |
| [Create Recipient](actions/create-recipient.md) | `POST /v1/recipients` | [docs](https://developers.trolley.com/api/#create-a-recipient) |
| [Create Recipient Account](actions/create-recipient-account.md) | `POST /v1/recipients/:id/accounts` | [docs](https://developers.trolley.com/api/#create-account) |
| [Create Recipient Offline Payment](actions/create-recipient-offline-payment.md) | `POST /v1/recipients/:id/offlinePayments` | [docs](https://developers.trolley.com/api/#create-an-offline-payment) |
| [Delete Invoice](actions/delete-invoice.md) | `POST /v1/invoices/delete` | [docs](https://developers.trolley.com/api/#delete-an-invoice) |
| [Delete Invoice Lines](actions/delete-invoice-lines.md) | `POST /v1/invoices/delete-lines` | [docs](https://developers.trolley.com/api/#delete-an-invoice-line) |
| [Delete Recipient](actions/delete-recipient.md) | `DELETE /v1/recipients/:id` | [docs](https://developers.trolley.com/api/#delete-a-recipient) |
| [Delete Recipient Account](actions/delete-recipient-account.md) | `DELETE /v1/recipients/:id/accounts/:recipientAccountId` | [docs](https://developers.trolley.com/api/#delete-account) |
| [Delete Recipient Offline Payment](actions/delete-recipient-offline-payment.md) | `DELETE /v1/recipients/:recipientId/offlinePayments/:offlinePaymentId` | [docs](https://developers.trolley.com/api/#delete-an-offline-payment) |
| [Get Country](actions/get-country.md) | `GET /v1/geography/countries/:code` | [docs](https://developers.trolley.com/api/#retrieve-a-country) |
| [Get Invoice](actions/get-invoice.md) | `POST /v1/invoices/get` | [docs](https://developers.trolley.com/api/#get-invoice) |
| [Get Recipient](actions/get-recipient.md) | `GET /v1/recipients/:id` | [docs](https://developers.trolley.com/api/#retrieve-a-recipient) |
| [Get Recipient Account](actions/get-recipient-account.md) | `GET /v1/recipients/:id/accounts/:recipientAccountId` | [docs](https://developers.trolley.com/api/#retrieve-account) |
| [Get Recipient Verifications](actions/get-recipient-verifications.md) | `POST /v1/verifications/get` | [docs](https://developers.trolley.com/api/#getting-verification-results) |
| [List Balances](actions/list-balances.md) | `GET /v1/balances` | [docs](https://developers.trolley.com/api/#retrieve-all-account-balances) |
| [List Batches](actions/list-batches.md) | `GET /v1/batches` | [docs](https://developers.trolley.com/api/#list-all-batches) |
| [List Offline Payments](actions/list-offline-payments.md) | `GET /v1/offline-payments` | [docs](https://developers.trolley.com/api/#list-all-offline-payments) |
| [List PayPal Account Balances](actions/list-pay-pal-account-balances.md) | `GET /v1/balances/paypal` | [docs](https://developers.trolley.com/api/#retrieve-paypal-account-balance) |
| [List Recipient Accounts](actions/list-recipient-accounts.md) | `GET /v1/recipients/:id/accounts` | [docs](https://developers.trolley.com/api/#recipients-and-recipient-accounts) |
| [List Recipient Logs](actions/list-recipient-logs.md) | `GET /v1/recipients/:id/logs` | [docs](https://developers.trolley.com/api/#retrieve-all-logs) |
| [List Recipient Offline Payments](actions/list-recipient-offline-payments.md) | `GET /v1/recipients/:id/offlinePayments` | [docs](https://developers.trolley.com/api/#retrieve-recipients-offline-payments) |
| [List Recipient Payments](actions/list-recipient-payments.md) | `GET /v1/recipients/:id/payments` | [docs](https://developers.trolley.com/api/#retrieve-all-payments) |
| [List Recipients](actions/list-recipients.md) | `GET /v1/recipients` | [docs](https://developers.trolley.com/api/#list-all-recipients) |
| [List Trolley Account Balances](actions/list-trolley-account-balances.md) | `GET /v1/balances/paymentrails` | [docs](https://developers.trolley.com/api/#retrieve-trolley-account-balance) |
| [List Verifications](actions/list-verifications.md) | `GET /v1/verifications` | [docs](https://developers.trolley.com/api/#list-all-verifications) |
| [Search Invoice Payments](actions/search-invoice-payments.md) | `POST /v1/invoices/payment/search` | [docs](https://developers.trolley.com/api/#search-invoice-payments) |
| [Search Invoices](actions/search-invoices.md) | `POST /v1/invoices/search` | [docs](https://developers.trolley.com/api/#search-invoices) |
| [Search Recipients](actions/search-recipients.md) | `GET /v1/recipients` | [docs](https://developers.trolley.com/api/#search-filter-recipients) |
| [Update Invoice](actions/update-invoice.md) | `POST /v1/invoices/update` | [docs](https://developers.trolley.com/api/#update-an-invoice) |
| [Update Invoice Lines](actions/update-invoice-lines.md) | `POST /v1/invoices/update-lines` | [docs](https://developers.trolley.com/api/#update-invoice-lines) |
| [Update Recipient](actions/update-recipient.md) | `PATCH /v1/recipients/:id` | [docs](https://developers.trolley.com/api/#update-a-recipient) |
