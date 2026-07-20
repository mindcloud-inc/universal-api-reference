# Update Project with BugHerd

Updates an existing project in BugHerd.

## Endpoint

- **Method:** `PUT`
- **Path:** `projects/:project_id.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [Update Project](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The BugHerd project ID. |
| `project` | body | `object` | no | Project fields to update. |
| `project.is_public` | body | `boolean` | no | Enable or disable public feedback. |
| `project.permission` | body | `string` | no | Guest visibility permission. |
