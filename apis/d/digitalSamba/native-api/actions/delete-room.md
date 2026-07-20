# Delete room with Digital Samba

Deletes an existing room from Digital Samba.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rooms/:room`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Delete room](https://developer.digitalsamba.com/rest-api/#rooms-DELETEapi-v1-rooms--room-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room` | path | `string` | yes | Room path parameter. |
| `body` | body | `object` | no | JSON request body documented for this endpoint. |
| `delete_resources` | body | `boolean` | no | If `true`, permanently deletes all session content for this room. Defaults to `false`. |
| `delete_history` | body | `boolean` | no | If `true`, anonymises PII for all archived participants of this room. Defaults to `false`. |
| `delete_library` | body | `boolean` | no | If `true`, deletes the room's content library. Defaults to `false`. |
