# Create Deployment with v0

Creates a new deployment in v0.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/deployments`
- **Base URL:** `https://api.v0.dev`
- **Official documentation:** [Create Deployment](https://v0.app/docs/api/platform/reference/deployments/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | body | `string` | yes | The project that owns the deployment. |
| `chatId` | body | `string` | yes | The chat to deploy. |
| `versionId` | body | `string` | yes | The chat version to deploy. |
