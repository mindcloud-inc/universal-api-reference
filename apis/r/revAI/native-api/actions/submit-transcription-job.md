# Submit Transcription Job with Rev AI

Creates a new transcription job in Rev AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/speechtotext/v1/jobs`
- **Base URL:** `https://api.rev.ai`
- **Official documentation:** [Submit Transcription Job](https://docs.rev.ai/api/asynchronous/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_config.url` | body | `string` | yes | Publicly accessible media URL to transcribe. |
| `metadata` | body | `string` | no | — |
| `transcriber` | body | `string` | no | Examples from docs: machine, low_cost, fusion, human. |
| `language` | body | `string` | no | — |
