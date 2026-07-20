# Update Project Member with Mendix

Updates a project team member in Mendix.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:projectId/members/:userId`
- **Base URL:** `https://projects-api.home.mendix.com/v2`
- **API:** rest
- **Official documentation:** [Update Project Member](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project-id` | path | `string` | yes | The unique identifier of a project. |
| `user-id` | path | `string` | yes | The unique identifier of a user. |
| `attributes[]` | body | `array<object>` | no | Array of member attributes to change. Documented keys include roleId, isPinned, and isWatching. |
