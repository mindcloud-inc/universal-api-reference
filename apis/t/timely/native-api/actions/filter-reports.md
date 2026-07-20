# Filter Reports with Timely

Retrieves filtered reports from Timely.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.1/{account_id}/reports/filter`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Filter Reports](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID |
| `since` | query | `date` | no | Start date for the report period (ISO 8601 format: YYYY-MM-DD) |
| `until` | query | `date` | no | End date for the report period (ISO 8601 format: YYYY-MM-DD) |
| `user_ids` | query | `string` | no | Comma-separated list of user IDs to filter by |
| `project_ids` | query | `string` | no | Comma-separated list of project IDs to filter by |
| `client_ids` | query | `string` | no | Comma-separated list of client IDs to filter by |
| `label_ids` | query | `string` | no | Comma-separated list of label IDs to filter by |
| `team_ids` | query | `string` | no | Comma-separated list of team IDs to filter by (requires teams feature) |
| `state_ids` | query | `string` | no | Comma-separated list of state IDs to filter by |
| `group_by` | query | `string` | no | Comma-separated list of grouping keys: clients, users, labels, days, teams. Default: all groups |
| `scope` | query | `string` | no | Result scope: totals (aggregated data) or events (individual entries). Default: totals |
| `billed` | query | `string` | no | Filter by billed status |
