# Get Action Options with Stack AI

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/options`
- **Base URL:** `https://api.stack-ai.com`
- **Official documentation:** [Get Action Options](https://docs.stackai.com/api-reference/tools#post-tools-options)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `config_name` | body | `string` | yes | The config field whose options should be fetched. |
| `provider_id` | body | `string` | yes | The provider identifier. |
| `action_id` | body | `string` | no | The action identifier. |
| `trigger_id` | body | `string` | no | The trigger identifier. |
| `connection_id` | body | `string` | no | The connection identifier. |
| `parameters` | body | `object` | no | Additional parameter values used to resolve dependent options. |
