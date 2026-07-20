# Create Project User Tag with Openlayer

Creates a new user tag for a project in Openlayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/user-tags`
- **Base URL:** `https://api.openlayer.com/v1`
- **Official documentation:** [Create Project User Tag](https://api.openlayer.com/v1/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `string` | yes | The tag color. |
| `name` | body | `string` | yes | The name of the user tag. |
| `projectId` | path | `string` | yes | The Openlayer project ID. |
