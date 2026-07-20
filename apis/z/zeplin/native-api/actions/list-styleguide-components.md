# List Styleguide Components with Zeplin

Retrieves a list of styleguide components from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/styleguides/{styleguide_id}/components`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Styleguide Components](https://docs.zeplin.dev/reference/getstyleguidecomponents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `section_id` | query | `string` | no | Filter by section id |
| `sort` | query | `string` | no | Sort components by their `section` or their `created` date |
| `linked_project` | query | `string` | no | Reference project id |
| `linked_styleguide` | query | `string` | no | Reference styleguide id |
| `include_linked_styleguides` | query | `boolean` | no | Whether to include linked styleguides or not |
| `include_latest_version` | query | `boolean` | no | Whether to include the latest version data in the Component object |
