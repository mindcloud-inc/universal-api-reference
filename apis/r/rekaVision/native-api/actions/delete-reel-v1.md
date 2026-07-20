# Delete Reel (V1) with Reka Vision

Deletes a reel generation from Reka Vision.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/clips/:id`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [Delete Reel (V1)](https://docs.reka.ai/vision/api-reference/v-1/delete-reel-v-1-clips-id-delete)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `delete_input_video` | body | `boolean` | no |
