# Update Invoice with Starfish

Updates an existing invoice in Starfish.

## Endpoint

- **Method:** `PUT`
- **Path:** `/invoices/:invoice_id`
- **Base URL:** `https://api.camping.care/v21`
- **Official documentation:** [Update Invoice](https://documenter.getpostman.com/view/9467805/VUjQkj1d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_id` | path | `number` | yes | Invoice ID. |
| `meta[0]` | query | `string` | no | Invoice meta update payload. |
