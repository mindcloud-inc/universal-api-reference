# Midjourney List Tasks with CometAPI

Retrieves Midjourney tasks from CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/mj/task/list-by-condition`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Midjourney List Tasks](https://apidoc.cometapi.com/api/image/midjourney/task-fetching-api/list-by-condition)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes | Task identifiers to query. |
