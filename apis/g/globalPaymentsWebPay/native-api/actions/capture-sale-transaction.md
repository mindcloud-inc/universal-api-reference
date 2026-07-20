# Capture Sale Transaction with Global Payments WebPay

Updates a sale transaction by capturing it in Global Payments WebPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/transactions/{id}/capture`
- **Base URL:** `https://apis.globalpay.com/ucp`
- **Official documentation:** [Capture Sale Transaction](https://developer.globalpayments.com/api/transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Global Payments transaction ID. |
