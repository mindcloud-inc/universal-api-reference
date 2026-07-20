# Run Virtual Try-On from Files with api4ai

Runs virtual try-on from person and apparel files in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/virtual-try-on/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Run Virtual Try-On from Files](https://api4.ai/docs/virtual-try-on)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Person image file to use for the try-on request. |
| `image-apparel` | body | `file` | yes | Apparel image file for the try-on request. |
