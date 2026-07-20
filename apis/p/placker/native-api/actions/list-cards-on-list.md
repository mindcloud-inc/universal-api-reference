# List Cards On List with Placker

## Endpoint

- **Method:** `GET`
- **Path:** `/list/:list/card`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [List Cards On List](https://placker.com/docs/api/paths/list.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list` | path | `number` | yes | List ID. |
| `includeArchived` | query | `boolean` | no | Include archived cards in results. |
