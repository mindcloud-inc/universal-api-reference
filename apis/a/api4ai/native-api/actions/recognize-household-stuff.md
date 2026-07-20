# Recognize Household Stuff with api4ai

Recognizes household items from an image URL in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/household-stuff/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Recognize Household Stuff](https://api4.ai/docs/household-stuff)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Publicly reachable image URL to analyze. |
