# Save Avatar with Uwear.ai

Creates an avatar from a generation result in Uwear.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/avatar`
- **Base URL:** `https://api.uwear.ai`
- **Official documentation:** [Save Avatar](https://docs.dev.uwear.ai/operations/external_create_avatar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `avatar_description` | body | `string` | no | Optional avatar description. |
| `avatar_name` | body | `string` | yes | Avatar name. |
| `generation_result_id` | body | `number` | yes | Generation result ID to save as an avatar. |
