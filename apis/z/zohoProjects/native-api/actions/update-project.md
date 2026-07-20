# Update Project with Zoho Projects

Updates an existing project in Zoho Projects.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/portal/[:PORTALID]/projects/[:PROJECTID]`
- **Base URL:** `https://projectsapi.zoho.com/api/v3`
- **Official documentation:** [Update Project](https://projectsapi.zoho.com/api-docs#projects_update-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PORTALID` | path | `string` | yes | Portal identifier from Zoho Projects. |
| `PROJECTID` | path | `string` | yes | Project identifier from Zoho Projects. |
| `name` | body | `string` | no | Project name. |
| `description` | body | `string` | no | Project description. |
| `project_type` | body | `string` | no | Project type. Accepted values: active, template, archived. |
| `owner.zpuid` | body | `string` | no | ZPUID of the project owner. |
| `is_public_project` | body | `boolean` | no | Whether the project is public. |
| `start_date` | body | `string` | no | Project start date in YYYY-MM-DD format. |
| `end_date` | body | `string` | no | Project end date in YYYY-MM-DD format. |
| `completed_time` | body | `string` | no | Project completed time. |
| `status.id` | body | `string` | no | Project status identifier. |
| `layout.id` | body | `string` | no | Project layout identifier. |
| `added_via` | body | `string` | no | Source from which the project is added. Accepted values: web, api. |
| `is_rollup_project` | body | `boolean` | no | Whether the project is a roll-up project. |
| `color` | body | `string` | no | Project color. |
