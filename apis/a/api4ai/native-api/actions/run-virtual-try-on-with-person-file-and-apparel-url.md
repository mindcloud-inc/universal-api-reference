# Run Virtual Try-On with Person File and Apparel URL with api4ai

Runs virtual try-on from a person file and apparel URL in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/virtual-try-on/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Run Virtual Try-On with Person File and Apparel URL](https://api4.ai/docs/virtual-try-on)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Person image file to use for the try-on request. |
| `url-apparel` | body | `string` | yes | Publicly reachable apparel image URL for the try-on request. |
