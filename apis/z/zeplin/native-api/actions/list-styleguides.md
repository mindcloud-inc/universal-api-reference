# List Styleguides with Zeplin

Retrieves a list of styleguides from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/styleguides`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Styleguides](https://docs.zeplin.dev/reference/getstyleguides)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace` | query | `string` | no | Workspace of the styleguide, it can be `personal` or the id of organization |
| `status` | query | `string` | no | Filter by status |
| `linked_project` | query | `string` | no | Reference project id |
| `linked_styleguide` | query | `string` | no | Reference styleguide id |
