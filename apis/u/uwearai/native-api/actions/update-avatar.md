# Update Avatar with Uwear.ai

Updates an existing avatar in Uwear.ai.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/avatar/:avatar_id`
- **Base URL:** `https://api.uwear.ai`
- **Official documentation:** [Update Avatar](https://docs.dev.uwear.ai/operations/external_update_avatar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `avatar_description` | body | `string` | no | Updated avatar description. |
| `avatar_id` | path | `number` | yes | Avatar ID. |
| `avatar_name` | body | `string` | no | Updated avatar name. |
