# List Project Spacing Sections with Zeplin

Retrieves a list of project spacing sections from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/spacing_sections`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Project Spacing Sections](https://docs.zeplin.dev/reference/getprojectspacingsections)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
