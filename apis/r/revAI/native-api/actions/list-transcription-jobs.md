# List Transcription Jobs with Rev AI

Retrieves transcription jobs from Rev AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/speechtotext/v1/jobs`
- **Base URL:** `https://api.rev.ai`
- **Official documentation:** [List Transcription Jobs](https://docs.rev.ai/api/asynchronous/reference)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `limit` | query | `number` | no |
| `starting_after` | query | `string` | no |
