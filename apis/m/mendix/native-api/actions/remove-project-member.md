# Remove Project Member with Mendix

Removes a project team member from Mendix.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:projectId/members/:userId`
- **Base URL:** `https://projects-api.home.mendix.com/v2`
- **API:** rest
- **Official documentation:** [Remove Project Member](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project-id` | path | `string` | yes | The unique identifier of a project. |
| `user-id` | path | `string` | yes | The unique identifier of a user. |
