# Authenticate Project User with Viqeo

Authenticates a project user in Viqeo.

## Endpoint

- **Method:** `POST`
- **Path:** `/media-platform/v1/project/:projectId/user/:email/authenticate`
- **Base URL:** `https://api.viqeo.tv`
- **Official documentation:** [Authenticate Project User](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_e0bfa8f879)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project identifier from the path. |
| `email` | path | `string` | yes | Project user email address. |
