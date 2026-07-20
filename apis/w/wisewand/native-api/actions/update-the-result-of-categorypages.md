# Update the result of categorypages with Wisewand

Updates a category page result in Wisewand.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/categorypages/:id/output/:outputId`
- **Base URL:** `https://api.wisewand.ai`
- **Official documentation:** [Update the result of categorypages](https://api.wisewand.ai/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Wisewand path parameter `id`. |
| `outputId` | path | `string` | yes | Wisewand path parameter `outputId`. |
