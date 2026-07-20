# Finmo: Native API Reference

A consolidated summary of Finmo's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.finmo.net/reference
- **API base URL:** `https://api.finmo.net/v1/`

## Authentication

### Basic Auth

Use your Finmo access key as username and secret key as password.

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

[Official authentication documentation](https://docs.finmo.net/reference/authentication)

## Pagination

Use `limit` in the query string to set the page size (default 10). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /customer` | [docs](https://docs.finmo.net/reference/newcustomer-1) |
| [Create Payin](actions/create-payin.md) | `POST /payin` | [docs](https://docs.finmo.net/reference/createpayin-1) |
| [Create Payout](actions/create-payout.md) | `POST /payout` | [docs](https://docs.finmo.net/reference/createpayout-1) |
| [Create Payout Beneficiary](actions/create-payout-beneficiary.md) | `POST /payout-beneficiary` | [docs](https://docs.finmo.net/reference/newpayoutbeneficiarycompany-1) |
| [Create Payout Sender](actions/create-payout-sender.md) | `POST /payout-sender` | [docs](https://docs.finmo.net/reference/createpayoutsender) |
| [Create Refund](actions/create-refund.md) | `POST /refund` | [docs](https://docs.finmo.net/reference/createrefund-1) |
| [Create Virtual Account](actions/create-virtual-account.md) | `POST /virtual-account` | [docs](https://docs.finmo.net/reference/newvirtualaccount-1) |
| [Delete Virtual Account](actions/delete-virtual-account.md) | `DELETE /virtual-account/:virtual_account_id` | [docs](https://docs.finmo.net/reference/deletevirtualaccount-1) |
| [Disable Customer](actions/disable-customer.md) | `PATCH /customer/:customer_id/disable` | [docs](https://docs.finmo.net/reference/disablecustomer-1) |
| [Enable Customer](actions/enable-customer.md) | `PATCH /customer/:customer_id/enable` | [docs](https://docs.finmo.net/reference/enablecustomer-1) |
| [Get Customer](actions/get-customer.md) | `GET /customer/:customer` | [docs](https://docs.finmo.net/reference/getcustomerbyid-1) |
| [Get Virtual Account](actions/get-virtual-account.md) | `GET /virtual-account/:virtual_account_id` | [docs](https://docs.finmo.net/reference/getvirtualaccountbyid-1) |
| [List Customers](actions/list-customers.md) | `GET /customer` | [docs](https://docs.finmo.net/reference/getallcustomers-1) |
| [List Payins](actions/list-payins.md) | `GET /payin` | [docs](https://docs.finmo.net/reference/listallpayins-1) |
| [List Payout Beneficiaries](actions/list-payout-beneficiaries.md) | `GET /payout-beneficiary` | [docs](https://docs.finmo.net/reference/getallpayoutbeneficiary-1) |
| [List Payout Senders](actions/list-payout-senders.md) | `GET /payout-sender` | [docs](https://docs.finmo.net/reference/getallpayoutsender) |
| [List Payouts](actions/list-payouts.md) | `GET /payout` | [docs](https://docs.finmo.net/reference/listallpayouts-1) |
| [List Refunds](actions/list-refunds.md) | `GET /refund` | [docs](https://docs.finmo.net/reference/listallrefunds-1) |
| [List Virtual Accounts](actions/list-virtual-accounts.md) | `GET /virtual-account` | [docs](https://docs.finmo.net/reference/getallvirtualaccount-1) |
| [List Wallets](actions/list-wallets.md) | `GET /wallet` | [docs](https://docs.finmo.net/reference/getallwallets-1) |
| [Retrieve Payin](actions/retrieve-payin.md) | `GET /payin/:payin_id` | [docs](https://docs.finmo.net/reference/retrievepayin-1) |
| [Retrieve Payout](actions/retrieve-payout.md) | `GET /payout/:payout_id` | [docs](https://docs.finmo.net/reference/retrievepayout-1) |
| [Retrieve Refund](actions/retrieve-refund.md) | `GET /refund/:refund_id` | [docs](https://docs.finmo.net/reference/retrieverefund-1) |
| [Update Customer](actions/update-customer.md) | `PATCH /customer/:customer_id` | [docs](https://docs.finmo.net/reference/updatecustomer-1) |
