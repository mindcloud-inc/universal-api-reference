# BlueSnap: Native API Reference

A consolidated summary of BlueSnap's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developers.bluesnap.com/
- **API base URL:** `https://sandbox.bluesnap.com/services/2`

## Authentication

### Basic Authentication

HTTP Basic authentication using BlueSnap API username and password from Merchant Portal Settings > API Settings.

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

[Official authentication documentation](https://developers.bluesnap.com/reference/authentication)

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Capture Authorized Transaction](actions/capture-authorized-transaction.md) | `PUT /transactions` | [docs](https://developers.bluesnap.com/v8976-JSON/reference/capture) |
| [Create Plan](actions/create-plan.md) | `POST /recurring/plans` | [docs](https://developers.bluesnap.com/v8976-JSON/reference/create-plan) |
| [Create Subscription](actions/create-subscription.md) | `POST /recurring/subscriptions` | [docs](https://developers.bluesnap.com/v8976-JSON/reference/create-subscription) |
| [Create Transaction](actions/create-transaction.md) | `POST /transactions` | [docs](https://developers.bluesnap.com/v8976-JSON/reference/auth-capture) |
| [Create Vaulted Shopper](actions/create-vaulted-shopper.md) | `POST /vaulted-shoppers` | [docs](https://developers.bluesnap.com/v8976-JSON/reference/create-vaulted-shopper) |
| [Delete Vaulted Shopper](actions/delete-vaulted-shopper.md) | `DELETE /vaulted-shoppers/:vaultedShopperId` | [docs](https://developers.bluesnap.com/v8976-JSON/reference/delete-vaulted-shopper) |
| [List Plans](actions/list-plans.md) | `GET /recurring/plans` | [docs](https://developers.bluesnap.com/v8976-JSON/reference/retrieve-all-plans) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /recurring/subscriptions` | [docs](https://developers.bluesnap.com/v8976-JSON/reference/retrieve-all-subscriptions) |
| [List Transactions](actions/list-transactions.md) | `GET /transactions` | [docs](https://developers.bluesnap.com/v8976-JSON/reference/retrieve) |
| [List Vaulted Shoppers](actions/list-vaulted-shoppers.md) | `GET /vaulted-shoppers` | [docs](https://developers.bluesnap.com/v8976-JSON/reference/retrieve-vaulted-shopper) |
| [Refund Transaction](actions/refund-transaction.md) | `POST /transactions/refund/:transactionId` | [docs](https://developers.bluesnap.com/v8976-JSON/reference/refund) |
| [Retrieve Card Info](actions/retrieve-card-info.md) | `POST /tools/credit-card-info-resolver` | [docs](https://developers.bluesnap.com/v8976-Tools/reference/retrieve-card-info) |
| [Retrieve Plan](actions/retrieve-plan.md) | `GET /recurring/plans/:planId` | [docs](https://developers.bluesnap.com/v8976-JSON/reference/retrieve-specific-plan) |
| [Retrieve Subscription](actions/retrieve-subscription.md) | `GET /recurring/subscriptions/:subscriptionId` | [docs](https://developers.bluesnap.com/v8976-JSON/reference/retrieve-specific-subscription) |
| [Retrieve Transaction](actions/retrieve-transaction.md) | `GET /transactions/:transactionId` | [docs](https://developers.bluesnap.com/v8976-JSON/reference/retrieve) |
| [Retrieve Vaulted Shopper](actions/retrieve-vaulted-shopper.md) | `GET /vaulted-shoppers/:vaultedShopperId` | [docs](https://developers.bluesnap.com/v8976-JSON/reference/retrieve-vaulted-shopper) |
| [Reverse Authorized Transaction](actions/reverse-authorized-transaction.md) | `PUT /transactions` | [docs](https://developers.bluesnap.com/v8976-JSON/reference/auth-reversal) |
| [Update Plan](actions/update-plan.md) | `PUT /recurring/plans/:planId` | [docs](https://developers.bluesnap.com/v8976-JSON/reference/update-plan) |
| [Update Subscription](actions/update-subscription.md) | `PUT /recurring/subscriptions/:subscriptionId` | [docs](https://developers.bluesnap.com/v8976-JSON/reference/update-subscription) |
| [Update Vaulted Shopper](actions/update-vaulted-shopper.md) | `PUT /vaulted-shoppers/:vaultedShopperId` | [docs](https://developers.bluesnap.com/v8976-JSON/reference/update-vaulted-shopper) |
