# Refund Sale Transaction with Global Payments WebPay

Creates a refund for a sale transaction in Global Payments WebPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/transactions/{id}/refund`
- **Base URL:** `https://apis.globalpay.com/ucp`
- **Official documentation:** [Refund Sale Transaction](https://developer.globalpayments.com/api/transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Global Payments transaction ID. |
