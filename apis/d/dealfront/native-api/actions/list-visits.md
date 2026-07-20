# List Visits with Dealfront

Retrieves visits from Dealfront.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:account_id/visits`
- **Base URL:** `https://api.leadfeeder.com`
- **Official documentation:** [List Visits](https://docs.leadfeeder.com/api/#get-all-visits)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | ID of the account whose visits you want to list. |
| `start_date` | query | `string` | yes | Start date for the visit search window in YYYY-MM-DD format. |
| `end_date` | query | `string` | yes | End date for the visit search window in YYYY-MM-DD format. |
