# Mirror Checklist Item To Card with Placker

## Endpoint

- **Method:** `POST`
- **Path:** `/checklist/:checklist/item/:item/mirror/card`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [Mirror Checklist Item To Card](https://placker.com/docs/api/paths/mirror.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklist` | path | `string` | yes | Source checklist ID. |
| `item` | path | `string` | yes | Source checklist item ID. |
| `list` | body | `number` | yes | Target list ID where the card will be created. |
| `title` | body | `string` | no | Optional title for the mirrored card. |
| `position` | body | `number` | no | Optional position within the list. |
| `description` | body | `string` | no | Optional description for the mirrored card. |
