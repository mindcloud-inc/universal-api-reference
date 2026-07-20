# List Comments with Langfuse

Retrieves comments from Langfuse.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [List Comments](https://api.reference.langfuse.com/#tag/Comments/GET/api/public/comments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `authorUserId` | query | `string` | no |
| `objectId` | query | `string` | no |
| `objectType` | query | `string` | no |
