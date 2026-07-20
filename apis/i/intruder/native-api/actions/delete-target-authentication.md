# Delete Target Authentication with Intruder

## Endpoint

- **Method:** `DELETE`
- **Path:** `/targets/:target_id/authentications/:id/`
- **Base URL:** `https://api.intruder.io/v1`
- **Official documentation:** [Delete Target Authentication](https://developers.intruder.io/reference/targets_authentications_destroy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_id` | path | `string` | yes | The Intruder target identifier. |
| `id` | path | `string` | yes | The Intruder target authentication identifier. |
