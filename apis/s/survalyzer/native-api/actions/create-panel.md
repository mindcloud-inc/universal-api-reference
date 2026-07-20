# Create Panel with Survalyzer

## Endpoint

- **Method:** `POST`
- **Path:** `/publicapi/Panel/v3/CreatePanel`
- **Base URL:** `https://api.survalyzer-eu.app`
- **Official documentation:** [Create Panel](https://developer.survalyzer.com/knowledge-base/public-api-eu/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Panel name. |
| `panelType` | body | `string` | no | Provider panel type to create. |
| `workspaceId` | body | `string` | no | Workspace where the panel should be created. |
