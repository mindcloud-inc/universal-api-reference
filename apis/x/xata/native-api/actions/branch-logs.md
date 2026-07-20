# Retrieve branch logs with Xata

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:organizationID/projects/:projectID/branches/:branchID/logs`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Retrieve branch logs](https://xata.io/docs/api-reference/branches/retrieve-branch-logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | — |
| `projectID` | path | `string` | yes | — |
| `branchID` | path | `string` | yes | — |
| `start` | body | `date` | yes | Start time |
| `end` | body | `date` | yes | End time |
| `filters[]` | body | `array` | no | Filters applied to log entries. Multiple filters are combined with AND. |
| `limit` | body | `number` | no | — |
| `cursor` | body | `string` | no | Pagination cursor from a previous response |
