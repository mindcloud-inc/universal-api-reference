# Anonymize Image with api4ai

Anonymizes an image from a URL in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/img-anonymization/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Anonymize Image](https://api4.ai/docs/image-anonymization)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Publicly reachable image URL to anonymize. |
