# Update Invoice with Alegra

Updates an existing sales invoice in Alegra.

## Endpoint

- **Method:** `PUT`
- **Path:** `/invoices/:id`
- **Base URL:** `https://api.alegra.com/api/v1`
- **Official documentation:** [Update Invoice](https://developer.alegra.com/reference/put_invoices-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `termsConditions` | body | `string` | no |
| `numberTemplate.id` | body | `string` | no |
| `numberTemplate.prefix` | body | `string` | no |
| `numberTemplate.number` | body | `string` | no |
| `items[].id` | body | `string` | no |
| `items[].name` | body | `string` | no |
| `items[].discount` | body | `number` | no |
| `items[].observations` | body | `string` | no |
| `items[].tax[].id` | body | `string` | no |
| `items[].price` | body | `number` | no |
| `items[].quantity` | body | `number` | no |
| `anotation` | body | `string` | no |
| `dueDate` | body | `string` | no |
| `date` | body | `string` | no |
| `observations` | body | `string` | no |
| `client.id` | body | `string` | no |
| `seller` | body | `number` | no |
| `priceList` | body | `number` | no |
| `currency` | body | `string` | no |
| `retentions[].id` | body | `string` | no |
| `retentions[].amount` | body | `number` | no |
| `warehouse` | body | `number` | no |
| `remissions[].id` | body | `string` | no |
| `remissions[].items[].id` | body | `string` | no |
| `costCenter` | body | `number` | no |
| `comments[]` | body | `array<string>` | no |
| `periodicity` | body | `string` | no |
