# List Styleguide Members with Zeplin

Retrieves a list of styleguide members from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/styleguides/{styleguide_id}/members`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Styleguide Members](https://docs.zeplin.dev/reference/getstyleguidemembers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `linked_project` | query | `string` | no | Reference project id |
| `linked_styleguide` | query | `string` | no | Reference styleguide id |
