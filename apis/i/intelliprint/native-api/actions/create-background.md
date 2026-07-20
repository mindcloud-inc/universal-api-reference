# Create Background with Intelliprint

## Endpoint

- **Method:** `POST`
- **Path:** `/backgrounds`
- **Base URL:** `https://api.intelliprint.net/v1`
- **Official documentation:** [Create Background](https://docs.intelliprint.net/api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Base64 string or file URL for the background artwork. |
| `name` | body | `string` | no | Optional background name. |
| `team` | body | `string` | no | Optional team ID to scope the background. |
