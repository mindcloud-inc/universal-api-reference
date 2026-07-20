# List Leaves with Trackabi

Retrieves company leave records from Trackabi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/leaves`
- **Base URL:** `https://api.trackabi.com`
- **Official documentation:** [List Leaves](https://trackabi.com/help/api-docs)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `date` | no | The start date for filtering records in YYYY-MM-DD format. |
| `end_date` | query | `date` | no | The end date for filtering records in YYYY-MM-DD format. |
| `own` | query | `number` | no | Set to 1 to return only leaves belonging to the API key owner. |
