# List Audit Logs with Statsig

Retrieves audit logs from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/audit_logs`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [List Audit Logs](https://docs.statsig.com/api-reference/audit-logs/list-audit-logs)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | — |
| `sortKey` | query | `string` | no | — |
| `sortOrder` | query | `string` | no | — |
| `latestID` | query | `string` | no | — |
| `tags` | query | `string` | no | — |
| `actionType` | query | `string` | no | — |
| `actionTypes` | query | `string` | no | — |
| `startDate` | query | `string` | no | Expected valid date in the form of YYYY-MM-DD. Defaults to 90 days before endDate. If both dates are omitted, the endpoint searches the last 90 days. |
| `endDate` | query | `string` | no | Expected valid date in the form of YYYY-MM-DD. Defaults to today. If both dates are omitted, the endpoint searches the last 90 days. |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
