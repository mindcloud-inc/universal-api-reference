# Create Prompt with Braintrust

Creates a new prompt in Braintrust.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/prompt`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Create Prompt](https://www.braintrust.dev/docs/api-reference/prompts/create-prompt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | Project id. |
| `name` | body | `string` | yes | Prompt name. |
| `slug` | body | `string` | yes | Prompt slug. |
