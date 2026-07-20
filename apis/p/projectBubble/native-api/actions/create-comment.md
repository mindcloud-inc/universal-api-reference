# Create Comment with Project Bubble

Creates a new comment in a Project Bubble project.

## Endpoint

- **Method:** `POST`
- **Path:** `/comments/:project_id`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Create Comment](https://help.proprofsproject.com/managing-comments)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `string` | yes |
| `comment` | body | `string` | yes |
