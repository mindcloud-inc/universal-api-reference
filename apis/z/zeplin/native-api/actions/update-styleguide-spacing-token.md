# Update Styleguide Spacing Token with Zeplin

Updates an existing styleguide spacing token in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/styleguides/{styleguide_id}/spacing_tokens/{spacing_token_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update Styleguide Spacing Token](https://docs.zeplin.dev/reference/updatestyleguidespacingtoken)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `spacing_token_id` | path | `string` | yes | Spacing token id |
| `name` | body | `string` | yes | The name of the token |
| `value` | body | `number` | yes | The value of the token |
