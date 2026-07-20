# Get Team Member with Tiledesk

Retrieves a team member from the current Tiledesk project.

## Endpoint

- **Method:** `GET`
- **Path:** `/{projectId}/project_users/users/:userId`
- **Base URL:** `https://api.tiledesk.com/v3`
- **Official documentation:** [Get Team Member](https://developer.tiledesk.com/apis/rest-api/team#get-the-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The teammate user identifier from the project. |
