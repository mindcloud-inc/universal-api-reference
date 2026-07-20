# Update Issue with Ninety.io

Updates an existing issue in Ninety.io.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/issues/:issueId`
- **Base URL:** `https://api.public.ninety.io`
- **Official documentation:** [Update Issue](https://api.public.ninety.io/v1/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issueId` | path | `string` | yes | The Issue Id |
| `title` | body | `string` | no | Title of the Issue |
| `teamId` | body | `string` | no | Id of the team that owns the Issue |
| `interval` | body | `string` | no | Interval classification for the Issue |
| `description` | body | `string` | no | HTML description of the Issue |
| `priority` | body | `number` | no | Priority of the Issue: 0-5 |
| `completed` | body | `boolean` | no | Whether the Issue is completed |
