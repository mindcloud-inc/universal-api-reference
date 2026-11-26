# List All Runs with MindCloud

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/runs`
- **Base URL:** `https://connect.mindcloud.co`
- **Official documentation:** [List All Runs](https://mindcloud.co/docs/api/rest/actions/list-all-runs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowId` | query | `list<string>` | no | Only runs of this workflow. |
| `status` | query | `list<string>` | no | Only runs with this status. Accepted values: `cancelled`, `cancelling`, `failed`, `finished`, `interrupted`, `limitExceeded`, `running`, `waiting`. |
| `from` | query | `string` | no | Only runs that started at or after this time, within the last 7 days: YYYY-MM-DD (midnight UTC) or an ISO 8601 date-time with a zone. Defaults to midnight UTC 7 days ago. |
