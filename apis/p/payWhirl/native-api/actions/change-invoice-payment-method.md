# Change Invoice Payment Method with PayWhirl

Changes an invoice's payment method in PayWhirl.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoice/{id}/card`
- **Base URL:** `https://api.paywhirl.com`
- **Official documentation:** [Change Invoice Payment Method](https://api.paywhirl.com/#invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The PayWhirl invoice ID. |
