# Save Custom Structure As Template with GatherContent

Creates a template from an item's custom structure in GatherContent.

## Endpoint

- **Method:** `POST`
- **Path:** `/items/:item_id/save_as_template`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Save Custom Structure As Template](https://docs.gathercontent.com/reference/savecustomstructureastemplate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_id` | path | `string` | yes | Item ID. |
| `name` | body | `string` | yes | Template name. |
