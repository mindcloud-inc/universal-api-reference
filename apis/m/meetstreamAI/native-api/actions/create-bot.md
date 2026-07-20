# Create Bot with Meetstream AI

Creates a new bot in Meetstream AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/create_bot`
- **Base URL:** `https://api.meetstream.ai/api/v1`
- **Official documentation:** [Create Bot](https://docs.meetstream.ai/api-reference/ap-is/bot-endpoints/create-bot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_link` | body | `string` | yes | The Google Meet, Zoom, or Teams meeting URL. |
| `bot_name` | body | `string` | yes | The display name the bot will use in the meeting. |
| `video_required` | body | `boolean` | no | Whether the bot should record video. |
| `join_at` | body | `date` | no | Schedule the bot to join at an ISO 8601 datetime. |
| `bot_message` | body | `string` | no | Optional initial message for the bot to post in meeting chat. |
| `callback_url` | body | `string` | no | Optional webhook URL for event callbacks. |
