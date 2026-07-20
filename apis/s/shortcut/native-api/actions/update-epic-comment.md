# Update Epic Comment with Shortcut

## Endpoint

- **Method:** `PUT`
- **Path:** `/epics/:epicPublicId/comments/:commentPublicId`
- **Base URL:** `https://api.app.shortcut.com/api/v3`
- **Official documentation:** [Update Epic Comment](https://developer.shortcut.com/api/rest/v3#Update-Epic-Comment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `epicPublicId` | path | `number` | yes |
| `commentPublicId` | path | `number` | yes |
| `text` | body | `string` | yes |
