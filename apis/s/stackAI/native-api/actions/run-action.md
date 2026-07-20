# Run Action with Stack AI

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/stackai/providers/:provider_id/actions/:action_id/run`
- **Base URL:** `https://api.stack-ai.com`
- **Official documentation:** [Run Action](https://docs.stackai.com/api-reference/tools#post-tools-stackai-providers-provider_id-actions-action_id-run)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action_id` | path | `string` | yes | The action identifier. |
| `provider_id` | path | `string` | yes | The provider identifier. |
| `project_id` | body | `string` | yes | The project identifier. |
| `inputs` | body | `object` | yes | The action inputs object. |
