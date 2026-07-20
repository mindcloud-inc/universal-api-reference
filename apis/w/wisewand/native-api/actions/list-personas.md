# List personas with Wisewand

Retrieves personas from your Wisewand workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/personas/`
- **Base URL:** `https://api.wisewand.ai`
- **Official documentation:** [List personas](https://api.wisewand.ai/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Wisewand query parameter `search`. |
| `extra_fields` | query | `object` | no | Wisewand query parameter `extra_fields`. |
