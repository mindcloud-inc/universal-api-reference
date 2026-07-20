# List Projects with Timing

Retrieves all project records from Timing.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://web.timingapp.com/api/v1`
- **Official documentation:** [List Projects](https://web.timingapp.com/docs/#projects-GETapi-v1-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | query | `string` | no | Filter projects whose title contains all words in this value. |
| `hide_archived` | query | `boolean` | no | Hide archived projects and their children from the results. |
| `team_id` | query | `string` | no | List projects for a specific team. Leave empty to list the user's private projects. |
