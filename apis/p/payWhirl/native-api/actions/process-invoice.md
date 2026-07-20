# Process Invoice with PayWhirl

Processes an invoice in PayWhirl.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoice/{id}/process`
- **Base URL:** `https://api.paywhirl.com`
- **Official documentation:** [Process Invoice](https://api.paywhirl.com/#invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The PayWhirl invoice ID. |
