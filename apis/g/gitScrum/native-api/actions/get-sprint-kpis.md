# Get Sprint KPIs with GitScrum

Retrieves KPI metrics for a GitScrum sprint.

## Endpoint

- **Method:** `GET`
- **Path:** `/sprints/:slug/kpis`
- **Base URL:** `https://services.gitscrum.com`
- **Official documentation:** [Get Sprint KPIs](https://docs.gitscrum.com/en/api/sprints)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_slug` | query | `string` | no |
| `project_slug` | query | `string` | no |
| `slug` | path | `string` | no |
