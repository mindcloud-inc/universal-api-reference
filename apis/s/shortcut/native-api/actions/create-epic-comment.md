# Create Epic Comment with Shortcut

## Endpoint

- **Method:** `POST`
- **Path:** `/epics/:epicPublicId/comments`
- **Base URL:** `https://api.app.shortcut.com/api/v3`
- **Official documentation:** [Create Epic Comment](https://developer.shortcut.com/api/rest/v3#Create-Epic-Comment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `epicPublicId` | path | `number` | yes |
| `text` | body | `string` | yes |
| `author_id` | body | `string` | no |
| `external_id` | body | `string` | no |
