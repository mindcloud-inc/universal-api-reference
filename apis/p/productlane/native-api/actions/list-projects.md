# List Projects with Productlane

Retrieves projects from a Productlane portal.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{workspaceId}`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [List Projects](https://productlane.mintlify.dev/docs/api/portal/list-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | Workspace ID to list public projects for. |
| `language` | query | `string` | no | Optional language override. |
