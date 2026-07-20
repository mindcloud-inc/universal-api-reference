# Download Chat Archive with ClickMeeting

Downloads a chat archive from ClickMeeting by session ID.

## Endpoint

- **Method:** `GET`
- **Path:** `chats/{{session_id}}`
- **Base URL:** `https://api.clickmeeting.com/v1`
- **Official documentation:** [Download Chat Archive](https://dev.clickmeeting.com/api-doc/#get_chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session_id` | path | `number` | yes | Session identifier used by the chat archive endpoint. |
