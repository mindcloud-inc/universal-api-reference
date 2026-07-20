# Label Image from File with api4ai

Labels an image from a file in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/general-cls/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Label Image from File](https://api4.ai/docs/image-labelling)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Image file to classify. |
