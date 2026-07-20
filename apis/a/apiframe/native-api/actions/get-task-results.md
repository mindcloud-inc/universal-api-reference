# Get Task Results with Apiframe

Retrieves multiple Apiframe task results by task IDs.

## Endpoint

- **Method:** `POST`
- **Path:** `/fetch-many`
- **Base URL:** `https://api.apiframe.pro`
- **Official documentation:** [Get Task Results](https://docs.apiframe.ai/api-endpoints/fetch-many)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task_ids[]` | body | `array<string>` | yes |
