# List Traces with Langfuse

Retrieves traces from Langfuse.

## Endpoint

- **Method:** `GET`
- **Path:** `/traces`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [List Traces](https://api.reference.langfuse.com/#tag/Trace/GET/api/public/traces)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `environment` | query | `string` | no |
| `fields` | query | `string` | no |
| `filter` | query | `string` | no |
| `fromTimestamp` | query | `string` | no |
| `name` | query | `string` | no |
| `orderBy` | query | `string` | no |
| `release` | query | `string` | no |
| `sessionId` | query | `string` | no |
| `tags` | query | `string` | no |
| `toTimestamp` | query | `string` | no |
| `userId` | query | `string` | no |
| `version` | query | `string` | no |
