# Update Stage with vPlan

## Endpoint

- **Method:** `PUT`
- **Path:** `/stage/[:id]`
- **Base URL:** `https://api.vplan.com/v1`
- **Official documentation:** [Update Stage](https://docs.api.vplan.com/stage.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Stage identifier. |
| `name` | body | `string` | yes | Stage name. |
