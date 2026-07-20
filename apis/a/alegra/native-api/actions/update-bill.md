# Update Bill with Alegra

Updates an existing purchase bill in Alegra.

## Endpoint

- **Method:** `PUT`
- **Path:** `/bills/:id`
- **Base URL:** `https://api.alegra.com/api/v1`
- **Official documentation:** [Update Bill](https://developer.alegra.com/reference/put_bills-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `date` | body | `string` | yes |
| `dueDate` | body | `string` | yes |
| `observations` | body | `string` | no |
| `termsConditions` | body | `string` | no |
| `provider` | body | `number` | yes |
| `numberTemplate.number` | body | `string` | no |
| `warehouse` | body | `number` | no |
| `purchases.items[].id` | body | `number` | no |
| `purchases.items[].name` | body | `string` | no |
| `purchases.items[].discount` | body | `number` | no |
| `purchases.items[].observations` | body | `string` | no |
| `purchases.items[].tax[].id` | body | `number` | no |
| `purchases.items[].tax[].name` | body | `string` | no |
| `purchases.items[].tax[].percentage` | body | `number` | no |
| `purchases.items[].tax[].description` | body | `string` | no |
| `purchases.items[].tax[].type` | body | `string` | no |
| `purchases.items[].tax[].status` | body | `string` | no |
| `purchases.items[].price` | body | `number` | no |
| `purchases.items[].quantity` | body | `number` | no |
| `purchases.items[].total` | body | `number` | no |
| `purchases.items[].subtotal` | body | `number` | no |
| `purchases.categories[].id` | body | `number` | no |
| `purchases.categories[].name` | body | `string` | no |
| `purchases.categories[].discount` | body | `number` | no |
| `purchases.categories[].observations` | body | `string` | no |
| `purchases.categories[].tax[].id` | body | `number` | no |
| `purchases.categories[].tax[].name` | body | `string` | no |
| `purchases.categories[].tax[].percentage` | body | `number` | no |
| `purchases.categories[].tax[].description` | body | `string` | no |
| `purchases.categories[].tax[].type` | body | `string` | no |
| `purchases.categories[].tax[].status` | body | `string` | no |
| `purchases.categories[].price` | body | `number` | no |
| `purchases.categories[].quantity` | body | `number` | no |
| `purchases.categories[].total` | body | `number` | no |
| `purchases.categories[].subtotal` | body | `number` | no |
| `retentions[].id` | body | `number` | no |
| `retentions[].amount` | body | `number` | no |
| `currency.code` | body | `string` | no |
| `currency.symbol` | body | `string` | no |
| `currency.exchangeRate` | body | `number` | no |
| `payments[].date` | body | `string` | no |
| `payments[].amount` | body | `number` | no |
| `payments[].account` | body | `string` | no |
| `payments[].paymentMethod` | body | `string` | no |
| `payments[].observations` | body | `string` | no |
| `payments[].anotation` | body | `string` | no |
| `payments[].retentions[].id` | body | `number` | no |
| `payments[].retentions[].name` | body | `string` | no |
| `payments[].retentions[].percentage` | body | `number` | no |
| `payments[].retentions[].amount` | body | `number` | no |
| `payments[].currency.code` | body | `string` | no |
| `payments[].currency.symbol` | body | `string` | no |
| `payments[].currency.exchangeRate` | body | `number` | no |
| `costCenter` | body | `number` | no |
