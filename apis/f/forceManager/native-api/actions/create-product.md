# Create Product with ForceManager

Creates a new product in ForceManager.

## Endpoint

- **Method:** `POST`
- **Path:** `/products`
- **Official documentation:** [Create Product](https://support.forcemanager.net/en/articles/8613478-entity-types)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Name of the product. |
| `price` | body | `number` | yes | Selling price for the product. |
| `category_id` | body | `number` | yes | ID of the category for the product. |
