# Remove People Background with api4ai

Removes a person's background from a URL in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/img-bg-removal/v1/people/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Remove People Background](https://api4.ai/docs/people-bg-removal)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Publicly reachable image URL to process. |
