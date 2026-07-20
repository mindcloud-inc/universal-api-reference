# Update the result of discoverarticles with Wisewand

Updates a discovery article result in Wisewand.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/discoverarticles/:id/output/:outputId`
- **Base URL:** `https://api.wisewand.ai`
- **Official documentation:** [Update the result of discoverarticles](https://api.wisewand.ai/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Wisewand path parameter `id`. |
| `outputId` | path | `string` | yes | Wisewand path parameter `outputId`. |
