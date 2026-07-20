# Get Project with Productlane

Retrieves a project from a Productlane portal.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{workspaceId}/{projectId}`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Get Project](https://productlane.mintlify.dev/docs/api/portal/get-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | Workspace ID to read the public project from. |
| `projectId` | path | `string` | yes | Project ID. |
| `language` | query | `string` | no | Optional language override. |
