# Add Project Member with Mendix

Adds a project team member in Mendix or sends an invitation.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/members`
- **Base URL:** `https://projects-api.home.mendix.com/v2`
- **API:** rest
- **Official documentation:** [Add Project Member](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project-id` | path | `string` | yes | The unique identifier of a project. |
| `memberId` | body | `string` | no | Unique identifier of the member to add to the project. |
| `roleId` | body | `string` | no | The unique identifier of the role assigned to the member. |
