# Create Screenshot with Localazy

Creates a new screenshot in a Localazy project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/screenshots`
- **Base URL:** `https://api.localazy.com`
- **Official documentation:** [Create Screenshot](https://localazy.com/docs/api/screenshot-management)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Localazy project identifier or slug. |
| `imageData` | body | `string` | yes | Image as a data URI, for example data:image/png;base64,... |
