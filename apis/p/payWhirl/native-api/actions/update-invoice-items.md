# Update Invoice Items with PayWhirl

Updates invoice line items in PayWhirl.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoice/{id}/items`
- **Base URL:** `https://api.paywhirl.com`
- **Official documentation:** [Update Invoice Items](https://api.paywhirl.com/#invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The PayWhirl invoice ID. |
