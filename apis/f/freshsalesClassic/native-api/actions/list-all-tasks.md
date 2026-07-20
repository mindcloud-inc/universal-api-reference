# List All Tasks with Freshsales Classic

Retrieves tasks from Freshsales Classic.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `https://{bundleAlias}/api`
- **Official documentation:** [List All Tasks](https://developers.freshworks.com/crm/api/#list_all_task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | yes | Freshsales task filter. Use one documented filter at a time, such as open, due_today, due_tomorrow, overdue, or completed. |
| `page` | query | `number` | no | Page number to return. |
