# Get the result of updateposts with Wisewand

Retrieves an update post result from Wisewand.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/updateposts/:id/output`
- **Base URL:** `https://api.wisewand.ai`
- **Official documentation:** [Get the result of updateposts](https://api.wisewand.ai/docs)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Wisewand path parameter `id`. |
| `outputId` | query | `string` | no | Wisewand query parameter `outputId`. |
