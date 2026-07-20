# Generate Session PDF Report with ClickMeeting

Generates a session PDF report in ClickMeeting.

## Endpoint

- **Method:** `GET`
- **Path:** `conferences/{{room_id}}/sessions/{{session_id}}/generate-pdf/{{lang}}`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [Generate Session PDF Report](https://dev.clickmeeting.com/api-doc/#get_generate_pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Conference room identifier. |
| `session_id` | path | `number` | yes | Session identifier. |
| `lang` | path | `string` | yes | Report language token from ClickMeeting. |
