# Update Checklist with Placker

## Endpoint

- **Method:** `PATCH`
- **Path:** `/checklist/:checklist`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [Update Checklist](https://placker.com/docs/api/paths/checklist.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklist` | path | `string` | yes | Checklist ID. |
| `title` | body | `string` | yes | New title of the checklist. |
