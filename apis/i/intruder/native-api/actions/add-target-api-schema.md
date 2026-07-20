# Add Target API Schema with Intruder

## Endpoint

- **Method:** `POST`
- **Path:** `/targets/:target_id/api_schemas/`
- **Base URL:** `https://api.intruder.io/v1`
- **Official documentation:** [Add Target API Schema](https://developers.intruder.io/reference/targets_api_schemas_create)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_id` | path | `string` | yes | Target ID. |
| `base_url` | body | `string` | yes | Base URL for the API schema. |
| `name` | body | `string` | yes | API schema name. |
| `target_authentication_id` | body | `number` | no | Related target authentication ID. |
| `file` | body | `file` | yes | API schema file upload. |
