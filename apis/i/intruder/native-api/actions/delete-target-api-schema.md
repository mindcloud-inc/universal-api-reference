# Delete Target API Schema with Intruder

## Endpoint

- **Method:** `DELETE`
- **Path:** `/targets/:target_id/api_schemas/:id/`
- **Base URL:** `https://api.intruder.io/v1`
- **Official documentation:** [Delete Target API Schema](https://developers.intruder.io/reference/targets_api_schemas_destroy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_id` | path | `string` | yes | The Intruder target identifier. |
| `id` | path | `string` | yes | The Intruder target API schema identifier. |
