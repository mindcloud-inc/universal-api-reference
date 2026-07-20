# Update Project Spacing Token with Zeplin

Updates an existing project spacing token in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/{project_id}/spacing_tokens/{spacing_token_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update Project Spacing Token](https://docs.zeplin.dev/reference/updateprojectspacingtoken)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `spacing_token_id` | path | `string` | yes | Spacing token id |
| `name` | body | `string` | yes | The name of the token |
| `value` | body | `number` | yes | The value of the token |
