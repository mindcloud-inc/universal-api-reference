# Find Deployments with v0

Finds deployments in the v0 workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/deployments`
- **Base URL:** `https://api.v0.dev`
- **Official documentation:** [Find Deployments](https://v0.app/docs/api/platform/reference/deployments/find)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | query | `string` | yes | The ID of the project to find deployments for. |
| `chatId` | query | `string` | yes | The ID of the chat to find deployments for. |
| `versionId` | query | `string` | yes | The ID of the version to find deployments for. |
