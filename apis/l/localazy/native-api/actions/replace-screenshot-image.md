# Replace Screenshot Image with Localazy

Updates an existing screenshot image in a Localazy project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/screenshots/:screenshotId`
- **Base URL:** `https://api.localazy.com`
- **Official documentation:** [Replace Screenshot Image](https://localazy.com/docs/api/screenshot-management)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Localazy project identifier or slug. |
| `screenshotId` | path | `string` | yes | Identifier of the screenshot to replace. |
| `imageData` | body | `string` | yes | Image as a data URI, for example data:image/png;base64,... |
