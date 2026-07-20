# Update Project Details with BrowserStack

Updates an existing project in BrowserStack Automate.

## Endpoint

- **Method:** `PUT`
- **Path:** `/automate/projects/:project_id.json`
- **Base URL:** `https://api.browserstack.com`
- **Official documentation:** [Update Project Details](https://www.browserstack.com/docs/automate/api-reference/selenium/project#update-project-details)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | BrowserStack project ID from List Projects. |
| `name` | body | `string` | yes | Updated BrowserStack project name. |
