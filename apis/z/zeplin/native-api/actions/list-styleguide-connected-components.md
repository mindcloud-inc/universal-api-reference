# List Styleguide Connected Components with Zeplin

Retrieves a list of styleguide connected components from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/styleguides/{styleguide_id}/connected_components`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Styleguide Connected Components](https://docs.zeplin.dev/reference/getstyleguideconnectedcomponents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `linked_project` | query | `string` | no | Reference project id |
| `linked_styleguide` | query | `string` | no | Reference styleguide id |
| `include_linked_styleguides` | query | `boolean` | no | Whether to include linked styleguides or not |
