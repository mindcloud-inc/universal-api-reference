# Parse Query with FTrack

Parses a query expression in FTrack.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `{serverUrl}`
- **Official documentation:** [Parse Query](https://developer.ftrack.com/api/operations/parse-query-api-parse-query-parsequery-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expression` | body | `string` | yes | ftrack query expression to parse. |
