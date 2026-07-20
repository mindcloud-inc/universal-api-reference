# Remove People Background from File with api4ai

Removes a person's background from a file in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/img-bg-removal/v1/people/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Remove People Background from File](https://api4.ai/docs/people-bg-removal)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | People image file to process. |
