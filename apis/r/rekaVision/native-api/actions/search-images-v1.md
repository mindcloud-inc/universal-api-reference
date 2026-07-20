# Search Images (V1) with Reka Vision

Finds images in Reka Vision by text query.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/images/search`
- **Base URL:** `https://vision-agent.api.reka.ai`
- **Official documentation:** [Search Images (V1)](https://docs.reka.ai/vision/api-reference/v-1/search-images-v-1-images-search-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | — |
| `max_results` | body | `number` | no | — |
| `search_mode` | body | `list<string>` | no | Accepted values: `joined`, `vision`. |
| `image_weight` | body | `number` | no | — |
| `text_weight` | body | `number` | no | — |
| `threshold` | body | `number` | no | — |
