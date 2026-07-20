# Update Item Structure with GatherContent

Updates the structure of an item in GatherContent.

## Endpoint

- **Method:** `PUT`
- **Path:** `/items/:item_id/structure`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Update Item Structure](https://docs.gathercontent.com/reference/updateitemstructure)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groups[]` | body | `array<object>` | yes | Structure groups definition. |
| `item_id` | path | `string` | yes | Item ID. |
