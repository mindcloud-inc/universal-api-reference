# Update Company with Salescamp

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/collections/69cd24c2f24a3ccfd974811e/items/:itemId`
- **Base URL:** `https://api.salescamp.app`
- **Official documentation:** [Update Company](https://developer.salescamp.app/reference/api-reference/items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemId` | path | `string` | yes | Resource ID of the company |
| `name` | body | `string` | no | Company name |
| `email` | body | `string` | no | Company email |
| `phone` | body | `string` | no | Company phone |
| `website` | body | `string` | no | Company website |
