# Run Virtual Try-On with Person URL and Apparel File with api4ai

Runs virtual try-on from a person URL and apparel file in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/virtual-try-on/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Run Virtual Try-On with Person URL and Apparel File](https://api4.ai/docs/virtual-try-on)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image-apparel` | body | `file` | yes | Apparel image file for the try-on request. |
| `url` | body | `string` | yes | Publicly reachable person image URL to use for the try-on request. |
