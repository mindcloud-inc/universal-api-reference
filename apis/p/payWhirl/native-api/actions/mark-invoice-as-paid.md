# Mark Invoice As Paid with PayWhirl

Marks an invoice as paid in PayWhirl.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoice/{id}/mark-as-paid`
- **Base URL:** `https://api.paywhirl.com`
- **Official documentation:** [Mark Invoice As Paid](https://api.paywhirl.com/#invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The PayWhirl invoice ID. |
