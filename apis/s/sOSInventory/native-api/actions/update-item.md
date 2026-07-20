# Update Item with SOS Inventory

Updates an existing item in SOS Inventory.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/item/:id`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [Update Item](https://developer.sosinventory.com/apidoc/Item)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Unique identifier for this record. |
| `syncToken` | body | `string` | yes | Current version token for this record. |
| `id` | body | `number` | yes | The item id echoed in the request body. |
| `name` | body | `string` | yes | The name of this item. |
| `type` | body | `string` | yes | The kind of item. |
| `description` | body | `string` | no | Default description of this item. |
| `sku` | body | `string` | no | Stockkeeping unit. |
| `notes` | body | `string` | no | Any relevant notes for this item. |
