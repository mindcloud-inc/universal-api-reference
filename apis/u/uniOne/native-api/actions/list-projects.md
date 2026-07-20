# List Projects with UniOne

Retrieves projects from UniOne, optionally by project ID.

## Endpoint

- **Method:** `POST`
- **Path:** `project/list.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [List Projects](https://docs.unione.io/en/web-api-ref#project-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | no | Optional project identifier to return only one project. |
