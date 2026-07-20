# Delete Conference with ClickMeeting

Deletes a conference from ClickMeeting by room ID.

## Endpoint

- **Method:** `DELETE`
- **Path:** `conferences/{{room_id}}`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [Delete Conference](https://dev.clickmeeting.com/api-doc/#delete_conferences_by_room_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Conference room identifier. |
