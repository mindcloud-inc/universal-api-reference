# List Project Spacing Tokens with Zeplin

Retrieves a list of project spacing tokens from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/spacing_tokens`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Project Spacing Tokens](https://docs.zeplin.dev/reference/getprojectspacingtokens)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `include_linked_styleguides` | query | `boolean` | no | Whether to include linked styleguides or not |
