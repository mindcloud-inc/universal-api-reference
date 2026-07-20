# Create Bot with Recallai

Creates a new bot in Recallai.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/bot/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [Create Bot](https://docs.recall.ai/reference/bot_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_name` | body | `string` | no | The name of the bot that will be displayed in the call. *(Note: Authenticated Google Meet bots will use the Google account name and this field will be ignored.)* |
| `join_at` | body | `string` | no | The time at which the bot will join the call, formatted in ISO 8601. This field can only be read from scheduled bots that have not yet joined a call. |
| `meeting_url` | body | `string` | yes | The url of the meeting. For example, https://zoom.us/j/123?pwd=456. This field will be cleared a few days after the bot has joined a call. |
