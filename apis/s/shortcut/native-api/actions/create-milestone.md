# Create Milestone with Shortcut

## Endpoint

- **Method:** `POST`
- **Path:** `/milestones`
- **Base URL:** `https://api.app.shortcut.com/api/v3`
- **Official documentation:** [Create Milestone](https://developer.shortcut.com/api/rest/v3#Create-Milestone)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `description` | body | `string` | no |
| `state` | body | `string` | no |
| `started_at_override` | body | `string` | no |
| `completed_at_override` | body | `string` | no |
