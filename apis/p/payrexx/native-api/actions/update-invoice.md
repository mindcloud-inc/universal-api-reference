# Update Invoice with Payrexx

Updates an invoice in Payrexx.

## Endpoint

- **Method:** `PATCH`
- **Path:** `Bill/:id/`
- **Base URL:** `https://api.payrexx.com/v1.14/`
- **Official documentation:** [Update Invoice](https://developers.payrexx.com/reference/update-an-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Invoice id. |
| `note` | body | `string` | yes | Invoice note text. |
