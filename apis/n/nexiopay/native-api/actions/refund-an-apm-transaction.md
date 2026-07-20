# Refund an APM transaction with Nexiopay

## Endpoint

- **Method:** `POST`
- **Path:** `/apm/v3/refund`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [Refund an APM transaction](https://docs.nexiopay.com/reference/refundapmtransaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Nexio APM payment ID to refund. |
| `data` | body | `object` | yes | APM refund data object documented by Nexio. |
