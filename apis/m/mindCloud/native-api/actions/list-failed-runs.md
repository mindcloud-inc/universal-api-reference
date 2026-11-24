# List Failed Runs with MindCloud

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/failed-runs`
- **Base URL:** `https://connect.mindcloud.co`
- **Official documentation:** [List Failed Runs](https://mindcloud.co/docs/api/rest/actions/list-failed-runs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowId` | query | `list<string>` | no | Only runs of this workflow. |
| `from` | query | `date` | no | Only runs that started at or after this time. |
| `before` | query | `date` | no | Only runs that started before this time. Leave empty for runs up to now. |
