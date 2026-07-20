# Reset Voice Messages with CallPage

Deletes all voice messages from CallPage.

## Endpoint

- **Method:** `POST`
- **Path:** `/voice/reset`
- **Base URL:** `https://core.callpage.io/api/v1/external`
- **Official documentation:** [Reset Voice Messages](https://callpage.github.io/documentation-rest/#reset-voice-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `widget_id` | body | `number` | yes | The widget identifier. |
| `message_id` | body | `list<string>` | no | The voice message identifier. Accepted values: `client.end_failed`, `client.end_success`, `client.start`, `manager.start`, `manager.start_manual`. |
