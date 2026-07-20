# List Styleguide Spacing Tokens with Zeplin

Retrieves a list of styleguide spacing tokens from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/styleguides/{styleguide_id}/spacing_tokens`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Styleguide Spacing Tokens](https://docs.zeplin.dev/reference/getstyleguidespacingtokens)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `linked_project` | query | `string` | no | Reference project id |
| `linked_styleguide` | query | `string` | no | Reference styleguide id |
| `include_linked_styleguides` | query | `boolean` | no | Whether to include linked styleguides or not |
