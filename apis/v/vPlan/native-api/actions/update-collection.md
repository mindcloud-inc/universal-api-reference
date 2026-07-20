# Update Collection with vPlan

## Endpoint

- **Method:** `PUT`
- **Path:** `/collection/[:id]`
- **Base URL:** `https://api.vplan.com/v1`
- **Official documentation:** [Update Collection](https://docs.api.vplan.com/collection.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Collection identifier. |
| `name` | body | `string` | yes | Collection name. |
