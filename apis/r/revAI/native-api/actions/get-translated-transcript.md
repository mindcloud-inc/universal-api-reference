# Get Translated Transcript with Rev AI

Retrieves a translated transcript from Rev AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/speechtotext/v1/jobs/:id/transcript/translation/:language`
- **Base URL:** `https://api.rev.ai`
- **Official documentation:** [Get Translated Transcript](https://docs.rev.ai/api/asynchronous/reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.rev.transcript.v1.0+json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `language` | path | `string` | yes |
