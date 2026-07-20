# Delete Checklist Item with Placker

## Endpoint

- **Method:** `DELETE`
- **Path:** `/checklist/:checklist/item/:item`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [Delete Checklist Item](https://placker.com/docs/api/paths/checklist.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklist` | path | `string` | yes | Checklist ID. |
| `item` | path | `string` | yes | Checklist item ID. |
