# Add Ticket Line Item with Syncro

Creates a ticket line item in Syncro.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:id/add_line_item`
- **Base URL:** `https://mindcloud.syncromsp.com/api/v1`
- **Official documentation:** [Add Ticket Line Item](https://api-docs.syncromsp.com/#/Ticket/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Syncro ticket ID. |
| `name` | body | `string` | yes | — |
| `upc_code` | body | `string` | no | — |
| `product_id` | body | `number` | no | — |
| `description` | body | `string` | yes | — |
| `quantity` | body | `number` | no | — |
| `price_cost` | body | `number` | no | — |
| `price_retail` | body | `number` | no | — |
| `taxable` | body | `boolean` | no | — |
