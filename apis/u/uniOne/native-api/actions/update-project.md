# Update Project with UniOne

Updates an existing project in UniOne.

## Endpoint

- **Method:** `POST`
- **Path:** `project/update.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Update Project](https://docs.unione.io/en/web-api-ref#project-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | Unique project identifier. |
| `project.name` | body | `string` | yes | Updated unique project name. |
