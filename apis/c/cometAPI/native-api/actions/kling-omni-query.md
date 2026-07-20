# Kling Omni Query with CometAPI

Retrieves a Kling Omni video task from CometAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/kling/v1/videos/omni-video/:task_id`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Kling Omni Query](https://apidoc.cometapi.com/api/video/kling/omni-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | Omni task identifier. |
