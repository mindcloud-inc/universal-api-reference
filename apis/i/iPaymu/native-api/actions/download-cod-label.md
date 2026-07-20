# Download COD Label with iPaymu

Download the shipping label for an iPaymu cash-on-delivery transaction.

## Endpoint

- **Method:** `GET`
- **Path:** `/cod/download-label/:transaction_id`
- **Base URL:** `https://my.ipaymu.com/api/v2`
- **Official documentation:** [Download COD Label](https://ipaymu.com/api-collection/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_id` | path | `string` | yes | COD transaction identifier. |
