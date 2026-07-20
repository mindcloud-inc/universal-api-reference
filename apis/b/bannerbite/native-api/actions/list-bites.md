# List Bites with Bannerbite

Retrieves bites from a Bannerbite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/bites`
- **Base URL:** `https://api.bannerbite.com`
- **Official documentation:** [List Bites](https://developer.bannerbite.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Number of bites to return. Bannerbite defaults to 10 and supports up to 100. |
| `project_id` | query | `number` | yes | The project ID whose bites you want to list. |
