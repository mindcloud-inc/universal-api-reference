# List Prompts with Langfuse

Retrieves prompts from Langfuse.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/prompts`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [List Prompts](https://api.reference.langfuse.com/#tag/Prompts/GET/api/public/v2/prompts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fromUpdatedAt` | query | `string` | no |
| `label` | query | `string` | no |
| `name` | query | `string` | no |
| `tag` | query | `string` | no |
| `toUpdatedAt` | query | `string` | no |
