# Get Translated Captions with Rev AI

Retrieves translated captions from Rev AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/speechtotext/v1/jobs/:id/captions/translation/:language`
- **Base URL:** `https://api.rev.ai`
- **Official documentation:** [Get Translated Captions](https://docs.rev.ai/api/asynchronous/reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/x-subrip` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `language` | path | `string` | yes |
