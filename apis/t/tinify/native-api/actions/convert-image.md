# Convert Image with Tinify

Converts an optimized image in Tinify.

## Endpoint

- **Method:** `POST`
- **Path:** `/output/:outputId`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Convert Image](https://tinify.com/developers/reference/http#converting-images)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputId` | path | `string` | yes | Tinify output identifier from a prior compression URL. |
| `convert.type` | body | `list` | yes | Target output MIME type. Accepted values: `0`, `1`, `2`, `3`, `4`. |
