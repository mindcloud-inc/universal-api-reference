# Get the result of categorypages with Wisewand

Retrieves a category page result from Wisewand.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/categorypages/:id/output`
- **Base URL:** `https://api.wisewand.ai`
- **Official documentation:** [Get the result of categorypages](https://api.wisewand.ai/docs)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Wisewand path parameter `id`. |
| `outputId` | query | `string` | no | Wisewand query parameter `outputId`. |
