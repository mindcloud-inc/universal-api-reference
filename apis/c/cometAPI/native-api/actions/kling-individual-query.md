# Kling Individual Query with CometAPI

Retrieves a Kling task from CometAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/kling/v1/:action/:action2/:task_id`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Kling Individual Query](https://apidoc.cometapi.com/api/video/kling/individual-queries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | path | `string` | yes | Kling resource group. |
| `action2` | path | `string` | yes | Kling sub-resource group. |
| `task_id` | path | `string` | yes | Kling task identifier. |
