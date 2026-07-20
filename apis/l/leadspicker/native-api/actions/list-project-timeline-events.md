# List Project Timeline Events with Leadspicker

Retrieves timeline events for a project in Leadspicker.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/sb/api/projects/:project_id/events`
- **Base URL:** `https://app.leadspicker.com`
- **Official documentation:** [List Project Timeline Events](https://app.leadspicker.com/app/sb/api/docs#/Project/apps_salesbooster_api_project_events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | Leadspicker project identifier. |
| `page` | query | `number` | no | Page number for timeline events. |
| `page_size` | query | `number` | no | Number of timeline events per page. |
| `search` | query | `string` | no | Search project timeline events. |
| `event_types` | query | `string<string>` | no | Comma-separated event types to include. |
