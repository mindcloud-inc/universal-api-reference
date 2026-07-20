# Update Project with zipBoard

Updates an existing project in zipBoard.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:id`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Update Project](https://help.zipboard.co/article/178-api-for-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collabemail` | body | `list<string>` | no | Optional collaborator email list. |
| `description` | body | `string` | no | Updated project description. |
| `id` | path | `string` | yes | Project record ID to update. |
| `projectid` | body | `string` | no | Updated custom project ID. |
| `title` | body | `string` | no | Updated project title. |
