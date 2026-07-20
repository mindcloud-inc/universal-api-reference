# Get Action by Provider and ID with Stack AI

## Endpoint

- **Method:** `GET`
- **Path:** `/tools/stackai/providers/:provider_id/actions/:action_id`
- **Base URL:** `https://api.stack-ai.com`
- **Official documentation:** [Get Action by Provider and ID](https://docs.stackai.com/api-reference/tools#get-tools-stackai-providers-provider_id-actions-action_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action_id` | path | `string` | yes | The action identifier. |
| `provider_id` | path | `string` | yes | The provider identifier. |
