# Create Comment with Uspacy

Creates a new comment in Uspacy.

## Endpoint

- **Method:** `POST`
- **Path:** `/comments/v1/comments`
- **Base URL:** `https://{site}`
- **Official documentation:** [Create Comment](https://uspacy.readme.io/reference/commentscontroller_createcomment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityType` | body | `string` | yes | The target entity type. |
| `entityId` | body | `number` | yes | The target entity ID. |
| `message` | body | `string` | yes | The comment message. |
