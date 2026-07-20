# Update Product Group with Digistore24

Updates an existing product group in Digistore24.

## Endpoint

- **Method:** `PUT`
- **Path:** `/updateProductGroup`
- **Base URL:** `https://www.digistore24.com/api/call`
- **Official documentation:** [Update Product Group](https://digistore24.com/api/docs/paths/updateProductGroup.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_group_id` | query | `number` | yes | Product group ID |
| `name` | body | `string` | no | Product group name |
| `position` | body | `number` | no | Display order |
| `is_shown_as_tab` | body | `boolean` | no | Display group as tab |
