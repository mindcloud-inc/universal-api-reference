# Generate Project Task List Report with Teamwork Projects

Generates a project task list report in Teamwork Projects.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{{projectId}}/tasklists.html`
- **Base URL:** `{apiEndPoint}projects/api/v3`
- **Official documentation:** [Generate Project Task List Report](https://apidocs.teamwork.com/docs/teamwork/v3/task-lists/get-projects-api-v3-projects-project-id-tasklists-html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Teamwork project ID. |
