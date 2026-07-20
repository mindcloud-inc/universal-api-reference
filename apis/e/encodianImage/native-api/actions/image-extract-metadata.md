# Image - Extract Metadata with Encodian - Image

Retrieves image metadata from Encodian - Image.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Image/GetImageInfo`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Image - Extract Metadata](https://support.encodian.com/hc/en-gb/articles/4431662425489)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | Base64 content of the source image file. |
| `simplifiedLatLongFormat` | body | `boolean` | no | Return latitude and longitude as formatted strings when location metadata is available. |
