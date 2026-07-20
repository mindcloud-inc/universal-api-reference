# List Project Text Styles with Zeplin

Retrieves a list of project text styles from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/text_styles`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Project Text Styles](https://docs.zeplin.dev/reference/getprojecttextstyles)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `include_linked_styleguides` | query | `boolean` | no | Whether to include linked styleguides or not |
