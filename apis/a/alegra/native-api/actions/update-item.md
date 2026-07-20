# Update Item with Alegra

Updates an existing item in Alegra.

## Endpoint

- **Method:** `PUT`
- **Path:** `/items/:id`
- **Base URL:** `https://api.alegra.com/api/v1`
- **Official documentation:** [Update Item](https://developer.alegra.com/reference/put_items-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
| `description` | body | `string` | no |
| `reference` | body | `string` | no |
| `price` | body | `number` | no |
| `category.id` | body | `string` | no |
| `inventory.unit` | body | `string` | no |
| `inventory.unitCost` | body | `number` | no |
| `inventory.negativeSale` | body | `boolean` | no |
| `inventory.warehouses[].id` | body | `string` | no |
| `inventory.warehouses[].initialQuantity` | body | `number` | no |
| `inventory.warehouses[].minQuantity` | body | `number` | no |
| `inventory.warehouses[].maxQuantity` | body | `number` | no |
| `tax` | body | `string` | no |
| `type` | body | `string` | no |
| `customFields[].id` | body | `string` | no |
| `customFields[].value` | body | `string` | no |
| `subitems[].item.id` | body | `string` | no |
| `subitems[].quantity` | body | `number` | no |
| `kitWarehouse.id` | body | `string` | no |
| `itemCategory.id` | body | `string` | no |
| `variantAttributes[].id` | body | `string` | no |
| `variantAttributes[].options[].id` | body | `string` | no |
| `accounting.inventory` | body | `string` | no |
| `accounting.inventariablePurchase` | body | `string` | no |
