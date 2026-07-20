# List Project People with Leadspicker

Retrieves people for a project in Leadspicker.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/sb/api/projects/:project_id/people`
- **Base URL:** `https://app.leadspicker.com`
- **Official documentation:** [List Project People](https://app.leadspicker.com/app/sb/api/docs#/Project%20Persons/apps_salesbooster_api_projects_people_list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | Leadspicker project identifier. |
| `page` | query | `number` | no | Page number for project people. |
| `page_size` | query | `number` | no | Number of project people per page. |
| `query` | query | `string` | no | Search project people. |
| `order_by` | query | `list<string>` | no | Sort project people by created or -created. Accepted values: `0`, `1`. |
