# Submit Topic Extraction Job with Rev AI

Creates a topic extraction job in Rev AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/topic_extraction/v1/jobs`
- **Base URL:** `https://api.rev.ai`
- **Official documentation:** [Submit Topic Extraction Job](https://docs.rev.ai/api/topic-extraction/reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `text` | body | `string` | yes |
| `metadata` | body | `string` | no |
| `language` | body | `string` | no |
