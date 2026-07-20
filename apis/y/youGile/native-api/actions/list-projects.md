# List projects with YouGile

Retrieves a list of projects from YouGile.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [List projects](https://ru.yougile.com/api-v2#/operations/ProjectController_search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeDeleted` | query | `boolean` | no | Include deleted projects in the result. |
| `title` | query | `string` | no | Filter projects by title. |
