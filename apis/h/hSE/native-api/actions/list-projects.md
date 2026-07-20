# List Projects with 4HSE

Retrieves projects from 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/project/index`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [List Projects](https://docs.4hse.com/en/api/project/#operation-indexProject-post)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | body | `object` | no | Project filters. |
| `filter.name` | body | `string` | no | Search a project by company name. |
| `filter.status` | body | `string` | no | Filter by lifecycle status. |
| `filter.project_type` | body | `string` | no | Filter by project type. |
| `history` | body | `boolean` | no | Include historized entries when true. |
