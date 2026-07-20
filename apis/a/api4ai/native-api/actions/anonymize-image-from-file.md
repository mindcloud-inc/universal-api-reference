# Anonymize Image from File with api4ai

Anonymizes an image from a file in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/img-anonymization/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Anonymize Image from File](https://api4.ai/docs/image-anonymization)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Image file to anonymize. |
