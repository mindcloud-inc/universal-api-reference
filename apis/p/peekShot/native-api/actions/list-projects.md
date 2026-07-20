# List Projects with PeekShot

Retrieves projects from PeekShot with optional filtering.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://api.peekshot.com/api/v1`
- **Official documentation:** [List Projects](https://docs.peekshot.com/api-reference/get-projects-list-cbtu)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `string` | no | Page number for paginated results. |
| `limit` | query | `string` | no | Number of results per page. |
| `name` | query | `string` | no | Filter projects by name. |
