# Create Project with Morningmate

Creates a new project in Morningmate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects`
- **Base URL:** `https://api.morningmate.com`
- **Official documentation:** [Create Project](https://api.morningmate.com/docs/api/v1/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `registerId` | body | `string` | yes | Morningmate author user ID |
| `title` | body | `string` | yes | Project title |
| `description` | body | `string` | no | Project description |
