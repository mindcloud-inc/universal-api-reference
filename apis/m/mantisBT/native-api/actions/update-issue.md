# Update Issue with MantisBT

Updates an existing issue in MantisBT.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/issues/{issue_id}`
- **Base URL:** `{baseUrl}/api/rest`
- **Official documentation:** [Update Issue](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issue_id` | path | `number` | yes | ID of the issue to update |
| `summary` | body | `string` | yes | Updated issue summary |
