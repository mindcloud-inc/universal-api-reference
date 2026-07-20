# Remove Promo From Invoice with PayWhirl

Removes a promo code from a PayWhirl invoice.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoice/{id}/remove-promo`
- **Base URL:** `https://api.paywhirl.com`
- **Official documentation:** [Remove Promo From Invoice](https://api.paywhirl.com/#invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The PayWhirl invoice ID. |
