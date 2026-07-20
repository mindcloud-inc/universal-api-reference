# Query Proposals with serviceminder.io

Finds proposals in ServiceMinder by date range.

## Endpoint

- **Method:** `POST`
- **Path:** `/proposal/query`
- **Base URL:** `https://serviceminder.com/api`
- **Official documentation:** [Query Proposals](https://serviceminder.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FromDate` | body | `string` | no | Start date for proposal query. |
| `ThroughDate` | body | `string` | no | End date for proposal query. |
