# Add Project Client with BugHerd

Adds a client to a BugHerd project.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_id/add_guest.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [Add Project Client](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `user_id` | body | `number` | no |
| `email` | body | `string` | no |
