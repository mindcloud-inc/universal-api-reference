# Convert Image With Background with Tinify

Converts an optimized image and fills its background in Tinify.

## Endpoint

- **Method:** `POST`
- **Path:** `/output/:outputId`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Convert Image With Background](https://tinify.com/developers/reference/http#converting-images)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputId` | path | `string` | yes | Tinify output identifier from a prior compression URL. |
| `convert.type` | body | `list` | yes | Target output MIME type for a transparent image that needs a filled background. Accepted values: `0`. |
| `transform.background` | body | `string` | yes | Background color, either a hex color such as #000000, white, or black. |
