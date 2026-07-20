# List Projects with Localazy

Retrieves projects from Localazy.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://api.localazy.com`
- **Official documentation:** [List Projects](https://localazy.com/docs/api/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | query | `boolean` | no | Include organization feature and quota information in the response. |
| `languages` | query | `boolean` | no | Include languages and translation counts in the response. |
