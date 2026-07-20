# Monitor Issue with MantisBT

Adds monitoring to an issue in MantisBT.

## Endpoint

- **Method:** `POST`
- **Path:** `/issues/{issue_id}/monitors`
- **Base URL:** `{baseUrl}/api/rest`
- **Official documentation:** [Monitor Issue](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issue_id` | path | `number` | yes | ID of the issue to monitor |
