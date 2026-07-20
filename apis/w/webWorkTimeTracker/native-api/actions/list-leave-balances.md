# List Leave Balances with WebWork Time Tracker

Retrieves leave balances from WebWork Time Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/leaves/balances`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [List Leave Balances](https://api-docs.webwork-tracker.com/api/leaves/getleavebalances)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | query | `number` | yes | ID of the workspace. |
| `date_from` | query | `string` | yes | Start date for balance calculation in YYYY-MM-DD format. Required by the provider runtime validation. |
| `date_to` | query | `string` | yes | End date for balance calculation in YYYY-MM-DD format. Required by the provider runtime validation. |
