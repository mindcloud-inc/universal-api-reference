# Create Item with SOS Inventory

Creates an item in SOS Inventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/item`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [Create Item](https://developer.sosinventory.com/apidoc/Item)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of this item. |
| `type` | body | `string` | yes | The kind of item. |
| `description` | body | `string` | no | Default description of this item. |
| `sku` | body | `string` | no | Stockkeeping unit. |
| `notes` | body | `string` | no | Any relevant notes for this item. |
