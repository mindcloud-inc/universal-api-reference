# List Projects with actiTIME

Retrieves a list of projects from actiTIME.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [List Projects](https://www.actitime.com/api-documentation/projects-resource)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `boolean` | no | Filter archived vs active projects. |
| `customerIds` | query | `string` | no | Comma-separated customer ids to retrieve projects from. |
| `ids` | query | `string` | no | Comma-separated ids of projects to be returned. |
| `includeReferenced` | query | `string` | no | Comma-separated referenced objects to include. |
| `name` | query | `string` | no | Exact project name match, case-insensitive. |
| `sort` | query | `string` | no | Sorting tokens like +name or -created. |
| `words` | query | `string` | no | Return projects containing all given words in the name. |
