# List Project Component Sections with Zeplin

Retrieves a list of project component sections from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/component_sections`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Project Component Sections](https://docs.zeplin.dev/reference/getprojectcomponentsections)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `page_id` | query | `string` | no | Filter by page id |
