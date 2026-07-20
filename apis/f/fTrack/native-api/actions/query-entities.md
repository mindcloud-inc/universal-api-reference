# Query Entities with FTrack

Retrieves entities from FTrack using an expression.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `{serverUrl}`
- **Official documentation:** [Query Entities](https://developer.ftrack.com/api/operations/query-api-query-query-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expression` | body | `string` | yes | ftrack query expression to execute. |
