# Get Captions with Rev AI

Retrieves captions from Rev AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/speechtotext/v1/jobs/:id/captions`
- **Base URL:** `https://api.rev.ai`
- **Official documentation:** [Get Captions](https://docs.rev.ai/api/asynchronous/reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/x-subrip` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `speaker_channel` | query | `number` | no | Optional channel number to caption for jobs created with speaker channel separation. |
