# Run Virtual Try-On with api4ai

Runs virtual try-on from person and apparel URLs in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/virtual-try-on/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Run Virtual Try-On](https://api4.ai/docs/virtual-try-on)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Publicly reachable image URL to use for the try-on request. |
| `url-apparel` | body | `string` | yes | Publicly reachable apparel image URL for the try-on request. |
