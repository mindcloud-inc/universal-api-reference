# List Time Entries with Timely

Retrieves time entries from Timely.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.1/{account_id}/hours`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [List Time Entries](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID for the time entries you want to retrieve |
| `since` | query | `date` | no | Filter time entries from this date (inclusive). Both since and upto needs to be present |
| `upto` | query | `date` | no | Filter time entries up to this date (inclusive). Both since and upto needs to be present |
| `day` | query | `date` | no | Filter time entries for a specific date. Defaults to current date if omitted. Disregarded if since and upto is present |
| `hour_ids` | query | `string` | no | Comma-separated list of time entry IDs to filter by |
| `sort` | query | `string` | no | Field to sort by |
| `order` | query | `string` | no | Sort order |
| `project_id` | query | `number` | no | Filter by project ID |
| `user_id` | query | `number` | no | Filter by user ID |
