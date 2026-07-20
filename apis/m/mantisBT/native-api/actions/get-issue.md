# Get Issue with MantisBT

Retrieves an issue from MantisBT by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/issues/{issue_id}`
- **Base URL:** `{baseUrl}/api/rest`
- **Official documentation:** [Get Issue](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issue_id` | path | `number` | yes | ID of the issue to retrieve |
