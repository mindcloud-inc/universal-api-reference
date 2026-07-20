# Create Project with BugHerd

Creates a new project in BugHerd.

## Endpoint

- **Method:** `POST`
- **Path:** `projects.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [Create Project](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project` | body | `object` | no |
| `project.name` | body | `string` | yes |
| `project.devurl` | body | `string` | no |
| `project.is_active` | body | `boolean` | no |
| `project.is_public` | body | `boolean` | no |
| `project.guests_see_guests` | body | `boolean` | no |
