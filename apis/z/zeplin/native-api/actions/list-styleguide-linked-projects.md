# List Styleguide Linked Projects with Zeplin

Retrieves a list of styleguide linked projects from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/styleguides/{styleguide_id}/linked_projects`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Styleguide Linked Projects](https://docs.zeplin.dev/reference/getstyleguidelinkedprojects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
