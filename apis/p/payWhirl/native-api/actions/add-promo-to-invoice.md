# Add Promo To Invoice with PayWhirl

Adds a promo code to a PayWhirl invoice.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoice/{id}/add-promo`
- **Base URL:** `https://api.paywhirl.com`
- **Official documentation:** [Add Promo To Invoice](https://api.paywhirl.com/#invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The PayWhirl invoice ID. |
