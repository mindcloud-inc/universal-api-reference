# Create Preview Invoice with Stripe

## Endpoint

- **Method:** `POST`
- **Path:** `invoices/create_preview`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Create Preview Invoice](https://docs.stripe.com/api/invoices/create_preview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer` | body | `string` | no | — |
| `subscription` | body | `string` | no | — |
| `schedule` | body | `string` | no | — |
| `preview_mode` | body | `list` | no | Accepted values: `0`, `1`. |
