# Refund Transaction with PayTabs

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/request`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Refund Transaction](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-7-Manage-Transactions/HPP-Step-7-Refund-Transaction/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cart_id` | body | `string` | yes | Merchant cart or order identifier. |
| `cart_currency` | body | `string` | yes | Transaction currency. |
| `cart_amount` | body | `number` | yes | Transaction amount to refund. |
| `cart_description` | body | `string` | yes | Reason or description for the refund. |
| `tran_ref` | body | `string` | yes | Captured or sale PayTabs transaction reference. |
