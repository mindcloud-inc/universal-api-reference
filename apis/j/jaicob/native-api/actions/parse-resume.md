# Parse Resume with Jaicob

## Endpoint

- **Method:** `POST`
- **Path:** `/file/resume`
- **Base URL:** `https://api.jaicob.ai`
- **Official documentation:** [Parse Resume](https://developers.jaicob.ai/reference/parse_resume)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | query | `string` | no | Optional idempotency or trace identifier. |
| `resume` | body | `file` | yes | Resume file to parse. |
