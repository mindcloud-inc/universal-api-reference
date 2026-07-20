# List Sessions with Langfuse

Retrieves sessions from Langfuse.

## Endpoint

- **Method:** `GET`
- **Path:** `/sessions`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [List Sessions](https://api.reference.langfuse.com/#tag/Sessions/GET/api/public/sessions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `environment` | query | `string` | no |
| `fromTimestamp` | query | `string` | no |
| `toTimestamp` | query | `string` | no |
