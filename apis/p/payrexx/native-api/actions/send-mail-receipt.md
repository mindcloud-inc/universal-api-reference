# Send Mail Receipt with Payrexx

Sends a transaction receipt email from Payrexx.

## Endpoint

- **Method:** `POST`
- **Path:** `Transaction/:id/receipt`
- **Base URL:** `https://api.payrexx.com/v1.14/`
- **Official documentation:** [Send Mail Receipt](https://developers.payrexx.com/reference/send-mail-receipt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the transaction with a receipt. |
| `recipient` | body | `string` | yes | Email address of recipient. |
