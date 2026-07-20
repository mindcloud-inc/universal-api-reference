# Create Story Comment with Shortcut

## Endpoint

- **Method:** `POST`
- **Path:** `/stories/:storyPublicId/comments`
- **Base URL:** `https://api.app.shortcut.com/api/v3`
- **Official documentation:** [Create Story Comment](https://developer.shortcut.com/api/rest/v3#Create-Story-Comment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `storyPublicId` | path | `number` | yes |
| `text` | body | `string` | yes |
| `author_id` | body | `string` | no |
| `external_id` | body | `string` | no |
| `parent_id` | body | `number` | no |
