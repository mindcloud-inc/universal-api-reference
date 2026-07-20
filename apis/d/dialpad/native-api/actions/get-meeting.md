# Get Meeting with Dialpad

Retrieves detailed meeting information from Dialpad.

## Endpoint

- **Method:** `GET`
- **Path:** `/meetings/:id`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [Get Meeting](https://developers.dialpad.com/reference/meetingsget)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The meeting room's ID. |
| `user_id` | query | `number` | no | The Dialpad user's id. |
