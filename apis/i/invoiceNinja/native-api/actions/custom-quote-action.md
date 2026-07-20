# Custom Quote Action with Invoice Ninja

## Endpoint

- **Method:** `GET`
- **Path:** `/quotes/:id/:action`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Custom Quote Action](https://api-docs.invoicing.co/#tag/quotes/operation/actionQuote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Hashed quote ID. |
| `action` | path | `string` | yes | Deprecated per-quote action string, such as history, archive, convert_to_invoice, or download. |
