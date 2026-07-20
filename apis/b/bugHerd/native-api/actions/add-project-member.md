# Add Project Member with BugHerd

Adds a member to a BugHerd project.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_id/add_member.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [Add Project Member](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `user_id` | body | `number` | yes |
