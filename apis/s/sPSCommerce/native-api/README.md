# SPS Commerce: Native API Reference

A consolidated summary of SPS Commerce's API configuration and 10 documented operations.

- **API base URL:** `https://api.spscommerce.com/`

## Authentication

### Custom

### Credentials

- **Client ID:** `client_id` · required
- **Client Secret:** `client_secret` · required

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Follow the complete next-page URL returned by the API.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Transaction](actions/create-transaction.md) | `POST transactions/v5/data/:filePath` | [docs](https://developercenter.spscommerce.com/#/docs/transaction-api/v5-posting) |
| [Delete Transaction](actions/delete-transaction.md) | `DELETE transactions/v5/data/:filePath` | [docs](https://developercenter.spscommerce.com/#/docs/transaction-api/v5-deletion) |
| [Get Transaction](actions/get-transaction.md) | `GET transactions/v5/data/:filePath` | [docs](https://developercenter.spscommerce.com/#/docs/transaction-api/v5-getting) |
| [List Forms](actions/list-forms.md) | `GET v1/forms` | [docs](https://developercenter.spscommerce.com/#/docs/shipping-doc-api/packing_slips/get_all_packing_slip) |
| [List Packing Slip](actions/list-packing-slip.md) | `GET packing-slip/v1/:slipID` | [docs](https://developercenter.spscommerce.com/#/docs/shipping-doc-api/packing_slips/get_all_packing_slip) |
| [List Packing Slips](actions/list-packing-slips.md) | `GET packing-slip/v1/` | [docs](https://developercenter.spscommerce.com/#/docs/shipping-doc-api/packing_slips/get_all_packing_slip) |
| [List Shipping Label by ID](actions/list-shipping-label.md) | `GET https://api.spscommerce.com/label/v1/:labelID` | [docs](https://developercenter.spscommerce.com/#/docs/shipping-doc-api/labels/get_labels_by_id) |
| [List Shipping Labels](actions/list-shipping-labels.md) | `GET https://api.spscommerce.com/label/v1/` | [docs](https://developercenter.spscommerce.com/#/docs/shipping-doc-api/labels/get_all_labels) |
| [List Transaction Histories](actions/list-transaction-histories.md) | `GET transactions/v5/history/` | [docs](https://developercenter.spscommerce.com/#/docs/transaction-api/v5-reporting) |
| [List Transactions](actions/list-transactions.md) | `GET transactions/v5/data/:directoryPath` | [docs](https://developercenter.spscommerce.com/#/docs/transaction-api/v5-filtering) |
