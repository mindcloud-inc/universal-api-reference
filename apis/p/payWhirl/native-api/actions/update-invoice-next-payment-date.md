# Update Invoice Next Payment Date with PayWhirl

Updates an invoice's next payment date in PayWhirl.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices/{id}/next-payment-date`
- **Base URL:** `https://api.paywhirl.com`
- **Official documentation:** [Update Invoice Next Payment Date](https://api.paywhirl.com/#invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The PayWhirl invoice ID. |
