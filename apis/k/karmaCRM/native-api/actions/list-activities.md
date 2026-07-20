# List Activities with Karma CRM

Retrieves a list of activities from Karma CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/activities.json`
- **Base URL:** `https://app.karmacrm.com`
- **Official documentation:** [List Activities](https://docs.karmacrm.com/#get-all-activities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to retrieve. |
| `per_page` | query | `number` | no | Number of activities per page. |
| `filters[due_category]` | query | `string` | no | Filter based on due_at date, for example overdue or today. |
| `filters[todo_category_id][values][]` | query | `array<number>` | no | Filter based on todo category IDs. |
| `filters[user_id]` | query | `string` | no | Filter by mine or a specific user ID. |
| `sorts[due_at]` | query | `string` | no | Sort due_at ascending asc or descending desc. |
| `columns[]` | query | `array<string>` | no | Columns to include in results, for example body or due_at. Send multiple values as a array. |
