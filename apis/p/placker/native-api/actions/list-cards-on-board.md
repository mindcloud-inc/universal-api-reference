# List Cards On Board with Placker

## Endpoint

- **Method:** `GET`
- **Path:** `/board/:board/card`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [List Cards On Board](https://placker.com/docs/api/paths/board.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board` | path | `number` | yes | Board ID. |
| `excludeArchived` | query | `boolean` | no | Exclude archived cards. |
