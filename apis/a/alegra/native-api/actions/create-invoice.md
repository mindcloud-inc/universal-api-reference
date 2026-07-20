# Create Invoice with Alegra

Creates a new sales invoice in Alegra.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices`
- **Base URL:** `https://api.alegra.com/api/v1`
- **Official documentation:** [Create Invoice](https://developer.alegra.com/reference/post_invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `termsConditions` | body | `string` | no | — |
| `numberTemplate.id` | body | `string` | no | — |
| `operationType` | body | `string` | no | Country-specific invoice versions may require an operation type. Peru accounts commonly use INTERNAL_SALE. |
| `numberTemplate.prefix` | body | `string` | no | — |
| `numberTemplate.number` | body | `string` | no | — |
| `items[].id` | body | `string` | no | — |
| `items[].name` | body | `string` | no | — |
| `items[].discount` | body | `number` | no | — |
| `items[].observations` | body | `string` | no | — |
| `items[].tax[].id` | body | `string` | no | — |
| `items[].price` | body | `number` | no | — |
| `items[].quantity` | body | `number` | no | — |
| `anotation` | body | `string` | no | — |
| `dueDate` | body | `string` | yes | — |
| `date` | body | `string` | yes | — |
| `observations` | body | `string` | no | — |
| `client.id` | body | `string` | yes | — |
| `seller` | body | `number` | no | — |
| `priceList` | body | `number` | no | — |
| `currency` | body | `string` | no | — |
| `retentions[].id` | body | `string` | no | — |
| `retentions[].amount` | body | `number` | no | — |
| `warehouse` | body | `number` | no | — |
| `remissions[].id` | body | `string` | no | — |
| `remissions[].items[].id` | body | `string` | no | — |
| `costCenter` | body | `number` | no | — |
| `comments[]` | body | `array<string>` | no | — |
| `periodicity` | body | `string` | no | — |
