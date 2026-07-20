# Send Call With Task (Simple) with Bland AI

Creates a task-based call in Bland AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/calls`
- **Base URL:** `https://api.bland.ai`
- **Official documentation:** [Send Call With Task (Simple)](https://docs.bland.ai/api-v1/post/calls-simple)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `phone_number` | body | `string` | yes |
| `task` | body | `string` | yes |
