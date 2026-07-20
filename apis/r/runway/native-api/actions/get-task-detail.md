# Get Task Detail with Runway

Retrieves task details from Runway.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/tasks/[:id]`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Get Task Detail](https://docs.dev.runwayml.com/api#tag/Task-management/paths/~1v1~1tasks~1%7Bid%7D/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of a previously submitted task. |
