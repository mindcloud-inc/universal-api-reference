# Update Scheduled Bot with Recallai

Updates a scheduled bot in Recallai.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/bot/:id/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [Update Scheduled Bot](https://docs.recall.ai/reference/bot_partial_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_name` | body | `string` | no | The name of the bot that will be displayed in the call. *(Note: Authenticated Google Meet bots will use the Google account name and this field will be ignored.)* |
| `id` | path | `string` | yes | A UUID string identifying this bot. |
| `join_at` | body | `string` | no | The time at which the bot will join the call, formatted in ISO 8601. This field can only be read from scheduled bots that have not yet joined a call. |
