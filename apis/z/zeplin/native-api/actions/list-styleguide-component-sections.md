# List Styleguide Component Sections with Zeplin

Retrieves a list of styleguide component sections from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/styleguides/{styleguide_id}/component_sections`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Styleguide Component Sections](https://docs.zeplin.dev/reference/getstyleguidecomponentsections)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `page_id` | query | `string` | no | Filter by page id |
| `linked_project` | query | `string` | no | Reference project id |
| `linked_styleguide` | query | `string` | no | Reference styleguide id |
