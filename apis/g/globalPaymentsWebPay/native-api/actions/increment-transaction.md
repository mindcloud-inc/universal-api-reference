# Increment Transaction with Global Payments WebPay

Updates a transaction by incrementing it in Global Payments WebPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/transactions/{id}/incremental`
- **Base URL:** `https://apis.globalpay.com/ucp`
- **Official documentation:** [Increment Transaction](https://developer.globalpayments.com/api/transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Global Payments transaction ID. |
