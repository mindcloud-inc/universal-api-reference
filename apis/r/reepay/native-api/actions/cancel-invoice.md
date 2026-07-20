# Cancel Invoice with Reepay

Cancels an invoice in Reepay.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/invoice/:id/cancel`
- **Base URL:** `https://api.frisbii.com`
- **Official documentation:** [Cancel Invoice](https://docs.frisbii.com/reference/cancelinvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Invoice identifier from Reepay. |
