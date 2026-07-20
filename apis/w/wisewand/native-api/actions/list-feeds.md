# List feeds with Wisewand

Retrieves feeds from your Wisewand workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/feeds/`
- **Base URL:** `https://api.wisewand.ai`
- **Official documentation:** [List feeds](https://api.wisewand.ai/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Wisewand query parameter `search`. |
| `status` | query | `string` | no | Wisewand query parameter `status`. |
| `project_id` | query | `string` | no | Wisewand query parameter `project_id`. |
