# List Projects with MILKEE

Retrieves projects from MILKEE.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/projects`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [List Projects](https://apidocs.milkee.ch/api/resources/projects.html#alle-projects-auflisten)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
