# Create Comment with Langfuse

Creates a comment in Langfuse.

## Endpoint

- **Method:** `POST`
- **Path:** `/comments`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [Create Comment](https://api.reference.langfuse.com/#tag/Comments/POST/api/public/comments)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `authorUserId` | body | `string` | no |
| `content` | body | `string` | no |
| `objectId` | body | `string` | no |
| `objectType` | body | `string` | no |
| `projectId` | body | `string` | no |
