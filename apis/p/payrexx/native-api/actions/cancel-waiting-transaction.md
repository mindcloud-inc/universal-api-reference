# Cancel Waiting Transaction with Payrexx

Cancels a waiting transaction in Payrexx.

## Endpoint

- **Method:** `PATCH`
- **Path:** `Transaction/:id/cancel`
- **Base URL:** `https://api.payrexx.com/v1.14/`
- **Official documentation:** [Cancel Waiting Transaction](https://developers.payrexx.com/reference/cancel-a-waiting-transaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of transaction to cancel. |
