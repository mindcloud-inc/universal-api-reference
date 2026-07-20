# Apply Template To Item with GatherContent

Applies a template to an item in GatherContent, replacing its fields.

## Endpoint

- **Method:** `POST`
- **Path:** `/items/:item_id/apply_template`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Apply Template To Item](https://docs.gathercontent.com/reference/applytemplate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_id` | path | `string` | yes | Item ID. |
| `template_id` | body | `string` | yes | Template ID to apply. |
