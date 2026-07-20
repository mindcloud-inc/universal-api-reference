# List Issues with Productlane

Retrieves issues from a Productlane portal.

## Endpoint

- **Method:** `GET`
- **Path:** `/issues/{workspaceId}`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [List Issues](https://productlane.mintlify.dev/docs/api/portal/list-issues)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | Workspace ID to list public issues for. |
| `language` | query | `string` | no | Optional language override. |
