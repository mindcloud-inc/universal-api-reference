# JVZoo: Native API Reference

A consolidated summary of JVZoo's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://api.jvzoo.com/docs/versions/v2.0.html
- **API base URL:** `https://api.jvzoo.com/v2.0`

## Authentication

### Basic Auth (API Key Username)

Use your JVZoo API key as the username and `x` as the password.

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

[Official authentication documentation](https://api.jvzoo.com/docs/versions/v2.0.html)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Recurring Payment](actions/cancel-recurring-payment.md) | `PUT /recurring_payment/:preKey` | [docs](https://api.jvzoo.com/docs/versions/v2.0.html#payments-recurring-payments-put) |
| [Get Affiliate Transactions](actions/get-affiliate-transactions.md) | `GET /latest-affiliates-transactions/[:paykey]` | [docs](https://api.jvzoo.com/docs/versions/v2.0.html#transactions-affiliate-transactions-get) |
| [Get Latest Transactions](actions/get-latest-transactions.md) | `GET /latest-transactions/[:paykey]` | [docs](https://api.jvzoo.com/docs/versions/v2.0.html#transactions-latest-transactions-get) |
| [Get Recurring Payment Status](actions/get-recurring-payment-status.md) | `GET /recurring_payment/:preKey` | [docs](https://api.jvzoo.com/docs/versions/v2.0.html#payments-recurring-payments-get) |
| [Get Transaction Summary](actions/get-transaction-summary.md) | `GET /transactions/summaries/:paykey` | [docs](https://api.jvzoo.com/docs/versions/v2.0.html#transactions-transaction-summaries-get) |
| [Retrieve Affiliate Status](actions/retrieve-affiliate-status.md) | `GET /products/:product_id/affiliates/:affiliate_id` | [docs](https://api.jvzoo.com/docs/versions/v2.0.html#affiliate-status-affiliate-status-get) |
