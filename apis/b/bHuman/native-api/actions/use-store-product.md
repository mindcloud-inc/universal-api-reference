# Use Store Product with BHuman

Creates a video instance from a store product in BHuman.

## Endpoint

- **Method:** `POST`
- **Path:** `https://store.bhuman.ai/api/store/product/use`
- **Base URL:** `https://studio.bhuman.ai/api`
- **Official documentation:** [Use Store Product](https://github.com/bhuman-ai/public_api#api-endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | body | `string` | no | Optional folder ID. |
| `id` | body | `string` | yes | The store product ID to use. |
| `video_instance_id` | body | `string` | no | Optional existing video instance ID. |
| `workspace_id` | body | `string` | yes | The target workspace ID. |
