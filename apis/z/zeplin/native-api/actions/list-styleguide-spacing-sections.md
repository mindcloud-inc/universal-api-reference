# List Styleguide Spacing Sections with Zeplin

Retrieves a list of styleguide spacing sections from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/styleguides/{styleguide_id}/spacing_sections`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Styleguide Spacing Sections](https://docs.zeplin.dev/reference/getstyleguidespacingsections)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `linked_project` | query | `string` | no | Reference project id |
| `linked_styleguide` | query | `string` | no | Reference styleguide id |
