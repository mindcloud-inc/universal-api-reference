# List Projects with Frameshift

Retrieves a list of projects from Frameshift.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [List Projects](https://mosaic.frameshift.io/api/#api-Projects-GetProjects)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | The project name to fuzzy search for |
