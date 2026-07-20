# List Project Design Tokens with Zeplin

Retrieves a list of project design tokens from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/design_tokens`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Project Design Tokens](https://docs.zeplin.dev/reference/getprojectdesigntokens)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `include_linked_styleguides` | query | `boolean` | no | Whether to include linked styleguides or not |
| `token_name_case` | query | `string` | no | Case for token names |
