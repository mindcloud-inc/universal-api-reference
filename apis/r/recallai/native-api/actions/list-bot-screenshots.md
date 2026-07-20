# List Bot Screenshots with Recallai

Retrieves bot screenshots from Recallai by bot ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/bot/:bot_id/screenshots/`
- **Base URL:** `https://{workspaceRegion}.recall.ai`
- **Official documentation:** [List Bot Screenshots](https://docs.recall.ai/reference/bot_screenshots_list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_id` | path | `string` | yes | The ID of the bot for which to retrieve the screenshots |
