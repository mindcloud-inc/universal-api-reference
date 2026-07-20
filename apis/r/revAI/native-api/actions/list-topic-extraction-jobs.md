# List Topic Extraction Jobs with Rev AI

Retrieves topic extraction jobs from Rev AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/topic_extraction/v1/jobs`
- **Base URL:** `https://api.rev.ai`
- **Official documentation:** [List Topic Extraction Jobs](https://docs.rev.ai/api/topic-extraction/reference)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `limit` | query | `number` | no |
| `starting_after` | query | `string` | no |
