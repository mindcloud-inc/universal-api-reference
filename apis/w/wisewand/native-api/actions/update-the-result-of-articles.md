# Update the result of articles with Wisewand

Updates an article result in Wisewand.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/articles/:id/output/:outputId`
- **Base URL:** `https://api.wisewand.ai`
- **Official documentation:** [Update the result of articles](https://api.wisewand.ai/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Wisewand path parameter `id`. |
| `outputId` | path | `string` | yes | Wisewand path parameter `outputId`. |
