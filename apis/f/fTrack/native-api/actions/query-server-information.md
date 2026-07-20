# Query Server Information with FTrack

Retrieves server information from FTrack.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `{serverUrl}`
- **Official documentation:** [Query Server Information](https://developer.ftrack.com/api/operations/query-server-information-api-query-server-information-queryserverinformation-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `values[]` | body | `array<string>` | no | Optional list of server-info keys to return. |
