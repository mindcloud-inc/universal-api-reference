# Update Deal with Salescamp

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/collections/69cd24c3f24a3ccfd974bb19/items/:itemId`
- **Base URL:** `https://api.salescamp.app`
- **Official documentation:** [Update Deal](https://developer.salescamp.app/reference/api-reference/items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemId` | path | `string` | yes | Resource ID of the deal |
| `name` | body | `string` | no | Deal name |
| `value` | body | `number` | no | Deal value |
| `status` | body | `string` | no | Deal status |
