# Update Board with vPlan

## Endpoint

- **Method:** `PUT`
- **Path:** `/board/[:id]`
- **Base URL:** `https://api.vplan.com/v1`
- **Official documentation:** [Update Board](https://docs.api.vplan.com/board.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Board identifier. |
| `name` | body | `string` | yes | Board name. |
