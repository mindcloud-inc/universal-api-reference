# List Comments with Uspacy

Retrieves all comment records from Uspacy.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments/v1/comments`
- **Base URL:** `https://{site}`
- **Official documentation:** [List Comments](https://uspacy.readme.io/reference/commentscontroller_getcomments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_type` | query | `string` | yes | Entity type name, for example post or task. |
| `entityId` | query | `number` | yes | The entity ID to load comments for. |
