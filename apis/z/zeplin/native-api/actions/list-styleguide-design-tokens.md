# List Styleguide Design Tokens with Zeplin

Retrieves a list of styleguide design tokens from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/styleguides/{styleguide_id}/design_tokens`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Styleguide Design Tokens](https://docs.zeplin.dev/reference/getstyleguidedesigntokens)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `include_linked_styleguides` | query | `boolean` | no | Whether to include linked styleguides or not |
| `token_name_case` | query | `string` | no | Case for token names |
