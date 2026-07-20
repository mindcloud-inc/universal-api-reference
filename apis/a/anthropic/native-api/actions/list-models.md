# List Models with Anthropic

Retrieves available API models from Anthropic.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/models`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [List Models](https://platform.claude.com/docs/en/api/models/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before_id` | query | `string` | no | Return results before this model ID. |
| `after_id` | query | `string` | no | Return results after this model ID. |
| `limit` | query | `number` | no | Number of items to return per page. |
