# List Access Tokens with ClickMeeting

Retrieves access tokens for a conference in ClickMeeting.

## Endpoint

- **Method:** `GET`
- **Path:** `conferences/{{room_id}}/tokens`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [List Access Tokens](https://dev.clickmeeting.com/api-doc/#get_tokens)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Conference room identifier. |
