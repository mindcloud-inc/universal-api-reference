# Create a question in the room with Digital Samba

Creates a room question in Digital Samba.

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms/:room/questions`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Create a question in the room](https://developer.digitalsamba.com/rest-api/#rooms-POSTapi-v1-rooms--room--questions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room` | path | `string` | yes | Room path parameter. |
| `body` | body | `object` | no | JSON request body documented for this endpoint. |
| `participant` | body | `object` | yes | Participant: either { "name", "external_id" } or { "id" } (uuid of existing participant). |
| `question` | body | `string` | yes | The question text. |
| `anonymous` | body | `boolean` | no | Whether to show as anonymous. |
| `breakout_id` | body | `string` | no | Must be a valid UUID. |
