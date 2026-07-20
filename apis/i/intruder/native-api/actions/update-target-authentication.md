# Update Target Authentication with Intruder

## Endpoint

- **Method:** `PATCH`
- **Path:** `/targets/:target_id/authentications/:id/`
- **Base URL:** `https://api.intruder.io/v1`
- **Official documentation:** [Update Target Authentication](https://developers.intruder.io/reference/targets_authentications_partial_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recorded_login_file` | body | `string` | no | Base64 data URI for a recorded login JSON file when type is recorded. |
| `target_id` | path | `string` | yes | The Intruder target identifier. |
| `id` | path | `string` | yes | The Intruder target authentication identifier. |
| `name` | body | `string` | no | A label for the target authentication. |
| `url` | body | `string` | no | The authenticated URL or login page used by the target authentication. |
| `type` | body | `string` | no | The Intruder authentication type. |
