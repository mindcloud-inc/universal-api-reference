# Update Target API Schema with Intruder

## Endpoint

- **Method:** `PATCH`
- **Path:** `/targets/:target_id/api_schemas/:id/`
- **Base URL:** `https://api.intruder.io/v1`
- **Official documentation:** [Update Target API Schema](https://developers.intruder.io/reference/targets_api_schemas_partial_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_id` | path | `string` | yes | Target ID. |
| `id` | path | `string` | yes | API schema ID. |
| `base_url` | body | `string` | no | Base URL for the API schema. |
| `name` | body | `string` | no | API schema name. |
| `target_authentication_id` | body | `number` | no | Related target authentication ID. |
| `file` | body | `file` | no | API schema file upload. |
