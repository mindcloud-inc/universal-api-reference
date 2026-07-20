# Create Checklist Item with Placker

## Endpoint

- **Method:** `POST`
- **Path:** `/checklist/:checklist/item`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [Create Checklist Item](https://placker.com/docs/api/paths/checklist.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklist` | path | `string` | yes | Checklist ID. |
| `title` | body | `string` | yes | Title of the checklist item. |
| `position` | body | `number` | no | Position of the item in the checklist. |
| `members[]` | body | `array<object>` | no | Members to assign to the item as an array of objects with id fields. |
