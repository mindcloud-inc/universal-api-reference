# Update Checklist Item with Placker

## Endpoint

- **Method:** `PATCH`
- **Path:** `/checklist/:checklist/item/:item`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [Update Checklist Item](https://placker.com/docs/api/paths/checklist.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklist` | path | `string` | yes | Checklist ID. |
| `item` | path | `string` | yes | Checklist item ID. |
| `title` | body | `string` | no | Title of the checklist item. |
| `description` | body | `string` | no | Description of the checklist item. |
| `status` | body | `string` | no | Status of the checklist item. |
| `startDates` | body | `object` | no | Planned and actual start dates. |
| `endDates` | body | `object` | no | Planned and actual end dates. |
| `effort` | body | `object` | no | Planned and actual effort values. |
| `duration` | body | `number` | no | Duration in seconds. |
| `trafficLight` | body | `string` | no | Traffic light status. |
| `membersAdd[]` | body | `array<object>` | no | Members to add to the item as an array of objects with id fields. |
| `membersRemove[]` | body | `array<object>` | no | Members to remove from the item as an array of objects with id fields. |
| `position` | body | `number` | no | Position of the item in the checklist. |
