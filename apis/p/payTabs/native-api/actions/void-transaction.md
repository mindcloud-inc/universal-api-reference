# Void Transaction with PayTabs

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/request`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Void Transaction](https://docs.paytabs.com/manuals/PT-API-Endpoints/Integration-Types-Manuals/Hosted-Payment-Page/HPP-Step-7-Manage-Transactions/HPP-Step-7-Void-Transaction/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cart_id` | body | `string` | yes | Merchant cart or order identifier. |
| `cart_currency` | body | `string` | yes | Transaction currency. |
| `cart_amount` | body | `number` | yes | Transaction amount to void. |
| `cart_description` | body | `string` | yes | Reason or description for the void. |
| `tran_ref` | body | `string` | yes | Authorized PayTabs transaction reference. |
