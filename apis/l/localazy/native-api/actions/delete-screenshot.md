# Delete Screenshot with Localazy

Deletes an existing screenshot from a Localazy project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:projectId/screenshots/:screenshotId`
- **Base URL:** `https://api.localazy.com`
- **Official documentation:** [Delete Screenshot](https://localazy.com/docs/api/screenshot-management)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Localazy project identifier or slug. |
| `screenshotId` | path | `string` | yes | Identifier of the screenshot to delete. |
