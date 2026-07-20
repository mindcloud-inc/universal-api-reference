# Mirror Card To Checklist Item with Placker

## Endpoint

- **Method:** `POST`
- **Path:** `/card/:card/mirror/item`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [Mirror Card To Checklist Item](https://placker.com/docs/api/paths/mirror.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `card` | path | `number` | yes | Source card ID. |
| `checklist` | body | `string` | yes | Target checklist ID. |
| `title` | body | `string` | no | Optional title for the mirrored item. |
| `position` | body | `number` | no | Optional position within the checklist. |
