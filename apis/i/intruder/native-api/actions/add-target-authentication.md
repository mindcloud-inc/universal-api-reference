# Add Target Authentication with Intruder

## Endpoint

- **Method:** `POST`
- **Path:** `/targets/:target_id/authentications/`
- **Base URL:** `https://api.intruder.io/v1`
- **Official documentation:** [Add Target Authentication](https://developers.intruder.io/reference/targets_authentications_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recorded_login_file` | body | `string` | no | Base64 data URI for a recorded login JSON file when type is recorded. |
| `target_id` | path | `string` | yes | The Intruder target identifier. |
| `name` | body | `string` | yes | A label for the target authentication. |
| `url` | body | `string` | yes | The authenticated URL or login page used by the target authentication. |
| `type` | body | `string` | yes | The Intruder authentication type. |
