# List Projects with GIRITON

Retrieves projects active on a selected GIRITON date.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/projects`
- **Base URL:** `https://rest.giriton.com/system/api`
- **Official documentation:** [List Projects](https://rest.giriton.com/apidoc/#/Projects/getProjects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dayFrom` | query | `string` | no | Starting date for included projects. |
| `departmentIds` | query | `string` | no | Comma-separated department IDs. |
| `dayTo` | query | `string` | no | End date for included projects. |
