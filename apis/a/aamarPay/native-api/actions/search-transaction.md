# Search Transaction with aamarPay

Retrieves transaction details from aamarPay by merchant transaction ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/trxcheck/request.php`
- **Base URL:** `https://sandbox.aamarpay.com`
- **Official documentation:** [Search Transaction](https://aamarpay.readme.io/reference/search-transaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | query | `string` | yes | Merchant transaction id or request id to search. |
