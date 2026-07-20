# Get Topic Extraction Result with Rev AI

Retrieves a topic extraction result from Rev AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/topic_extraction/v1/jobs/:id/result`
- **Base URL:** `https://api.rev.ai`
- **Official documentation:** [Get Topic Extraction Result](https://docs.rev.ai/api/topic-extraction/reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.rev.topic.v1.0+json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `threshold` | query | `number` | no |
