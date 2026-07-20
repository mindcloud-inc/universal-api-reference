# Create Issue with Zoho Projects

Creates a new issue in Zoho Projects.

## Endpoint

- **Method:** `POST`
- **Path:** `/portal/[:PORTALID]/projects/[:PROJECTID]/issues`
- **Base URL:** `https://projectsapi.zoho.com/api/v3`
- **Official documentation:** [Create Issue](https://projectsapi.zoho.com/api-docs#issues_create-an-issue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PORTALID` | path | `string` | yes | Zoho Projects portal ID. |
| `PROJECTID` | path | `string` | yes | Zoho Projects project ID. |
| `name` | body | `string` | yes | Issue title. |
| `description` | body | `string` | no | Issue description. |
| `flag` | body | `string` | no | Issue visibility flag. |
| `associated_teams.id` | body | `string` | no | Associated team ID. |
| `assignee.zpuid` | body | `string` | no | Assignee ZPUID. |
| `status.id` | body | `string` | no | Issue status ID. |
| `due_date` | body | `string` | no | Issue due date. |
| `release_milestone.id` | body | `string` | no | Release milestone ID. |
| `affected_milestone.id` | body | `string` | no | Affected milestone ID. |
| `severity.id` | body | `string` | no | Issue severity ID. |
| `is_it_reproducible.id` | body | `string` | no | Reproducible value ID. |
| `classification.id` | body | `string` | no | Issue classification ID. |
| `module.id` | body | `string` | no | Issue module ID. |
| `rate_per_hour` | body | `number` | no | Billing rate per hour. |
| `cost_rate_per_hour` | body | `number` | no | Cost rate per hour. |
