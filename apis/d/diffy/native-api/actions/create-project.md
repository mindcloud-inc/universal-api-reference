# Create Project with Diffy

Creates a new project in Diffy.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://app.diffy.website/api`
- **Official documentation:** [Create Project](https://app.diffy.website/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Project name. |
| `production` | body | `string` | yes | Production environment URL. |
