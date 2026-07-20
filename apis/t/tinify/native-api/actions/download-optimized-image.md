# Download Optimized Image with Tinify

Downloads an optimized image from Tinify.

## Endpoint

- **Method:** `GET`
- **Path:** `/output/:outputId`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Download Optimized Image](https://tinify.com/developers/reference/http#compressing-images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputId` | path | `string` | yes | Tinify output identifier from a prior compression URL. |
