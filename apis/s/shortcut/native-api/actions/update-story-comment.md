# Update Story Comment with Shortcut

## Endpoint

- **Method:** `PUT`
- **Path:** `/stories/:storyPublicId/comments/:storyCommentPublicId`
- **Base URL:** `https://api.app.shortcut.com/api/v3`
- **Official documentation:** [Update Story Comment](https://developer.shortcut.com/api/rest/v3#Update-Story-Comment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `storyPublicId` | path | `number` | yes |
| `storyCommentPublicId` | path | `number` | yes |
| `text` | body | `string` | yes |
