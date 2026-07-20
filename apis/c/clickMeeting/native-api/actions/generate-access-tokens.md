# Generate Access Tokens with ClickMeeting

Creates access tokens for a conference in ClickMeeting.

## Endpoint

- **Method:** `POST`
- **Path:** `conferences/{{room_id}}/tokens`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [Generate Access Tokens](https://dev.clickmeeting.com/api-doc/#post_tokens)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room_id` | path | `number` | yes | Conference room identifier. |
| `how_many` | body | `number` | yes | Number of access tokens to generate. |
