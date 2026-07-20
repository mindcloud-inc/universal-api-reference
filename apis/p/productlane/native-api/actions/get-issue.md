# Get Issue with Productlane

Retrieves an issue from a Productlane portal.

## Endpoint

- **Method:** `GET`
- **Path:** `/issues/{workspaceId}/{issueId}`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Get Issue](https://productlane.mintlify.dev/docs/api/portal/get-issue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | Workspace ID to read the public issue from. |
| `issueId` | path | `string` | yes | Issue ID. |
| `language` | query | `string` | no | Optional language override. |
