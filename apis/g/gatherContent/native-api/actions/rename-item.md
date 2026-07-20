# Rename Item with GatherContent

Renames an existing item in GatherContent.

## Endpoint

- **Method:** `POST`
- **Path:** `/items/:item_id/rename`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Rename Item](https://docs.gathercontent.com/reference/renameitem)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_id` | path | `string` | yes | Item ID. |
| `name` | body | `string` | yes | Item name. |
