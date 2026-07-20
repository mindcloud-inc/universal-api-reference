# Get Project Statistics with Leadspicker

Retrieves sequence statistics for a project in Leadspicker.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/sb/api/projects/:project_id/sequence-stats`
- **Base URL:** `https://app.leadspicker.com`
- **Official documentation:** [Get Project Statistics](https://app.leadspicker.com/app/sb/api/docs#/Project/apps_salesbooster_api_project_sequence_stats_detail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | Leadspicker project identifier. |
| `start_date` | query | `date` | no | Start date for project statistics in YYYY-MM-DD format. |
| `end_date` | query | `date` | no | End date for project statistics in YYYY-MM-DD format. |
