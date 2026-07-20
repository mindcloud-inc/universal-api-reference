# Get Report Totals with Timely

Retrieves report totals from Timely.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.1/{account_id}/reports`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Get Report Totals](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID |
| `since` | query | `date` | no | Start date for the report period (ISO 8601 format: YYYY-MM-DD) |
| `until` | query | `date` | no | End date for the report period (ISO 8601 format: YYYY-MM-DD) |
| `user_ids` | query | `string` | no | Comma-separated list of user IDs to filter by |
| `project_ids` | query | `string` | no | Comma-separated list of project IDs to filter by |
| `client_ids` | query | `string` | no | Comma-separated list of client IDs to filter by |
