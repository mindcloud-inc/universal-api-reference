# Update Voice Message with CallPage

Updates an existing voice message in CallPage.

## Endpoint

- **Method:** `POST`
- **Path:** `/voice/update`
- **Base URL:** `https://core.callpage.io/api/v1/external`
- **Official documentation:** [Update Voice Message](https://callpage.github.io/documentation-rest/#update-voice-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `widget_id` | body | `number` | yes | The widget identifier. |
| `message_id` | body | `list<string>` | yes | The voice message identifier. Accepted values: `client.end_failed`, `client.end_success`, `client.start`, `manager.start`, `manager.start_manual`. |
| `enabled` | body | `boolean` | yes | Whether the voice message should be enabled. |
| `file` | body | `string` | no | A public URL to an audio file. |
