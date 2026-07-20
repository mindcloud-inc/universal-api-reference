# Query Payments with serviceminder.io

Finds payments in ServiceMinder by date range.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/query`
- **Base URL:** `https://serviceminder.com/api`
- **Official documentation:** [Query Payments](https://serviceminder.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FromDate` | body | `date` | no | Start date for payment query. |
| `ThroughDate` | body | `date` | no | End date for payment query. |
