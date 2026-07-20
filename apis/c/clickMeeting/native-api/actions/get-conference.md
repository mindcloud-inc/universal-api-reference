# Get Conference with ClickMeeting

Retrieves a conference from ClickMeeting by room ID.

## Endpoint

- **Method:** `GET`
- **Path:** `conferences/{{room_id}}`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [Get Conference](https://dev.clickmeeting.com/api-doc/#get_conferences_by_room_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Conference room identifier. |
