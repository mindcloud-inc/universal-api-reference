# List Projects with Seven Time

Retrieves projects from a Seven Time workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://app.seventime.se/api/2`
- **Official documentation:** [List Projects](https://docs.seventime.se/#get-projects)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter projects by name. |
| `projectNumber` | query | `string` | no | Filter projects by project number. |
| `lastModified` | query | `date` | no | Include projects modified since the given timestamp. |
