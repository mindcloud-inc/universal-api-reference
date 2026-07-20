# Create Comment with ProProfs Project

Creates a new comment in ProProfs Project.

## Endpoint

- **Method:** `POST`
- **Path:** `/comments/{{project_id}}`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Create Comment](https://help.proprofsproject.com/managing-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment` | body | `string` | yes | The comment text. |
| `project_id` | path | `string` | yes | The project ID that will own the comment. |
