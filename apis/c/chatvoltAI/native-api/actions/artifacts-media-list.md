# List Media with Chatvolt AI

Retrieves media from Chatvolt AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/artifacts/media`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [List Media](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/media/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `artifact_id` | query | `string` | yes | — |
| `q` | query | `string` | no | Search by name or alt description. |
| `type` | query | `string` | no | — |
