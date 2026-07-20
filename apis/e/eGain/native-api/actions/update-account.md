# Update Account with eGain

Updates an existing account in eGain.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:id`
- **Base URL:** `https://api.ai.egain.cloud/conversation/conversationmgr/v3`
- **Official documentation:** [Update Account](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/account/updateaccount.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | yes | Whether account is active. |
| `address` | body | `string` | yes | Account address. |
| `channel.id` | body | `string` | yes | Channel ID. |
| `chatConfigurations.defaultLanguage` | body | `string` | no | Default language. |
| `chatConfigurations.entryPoint.id` | body | `string` | yes | Entry point ID. |
| `chatConfigurations.orchestration.id` | body | `string` | yes | Orchestration ID. |
| `chatConfigurations.timeout` | body | `number` | yes | Chat timeout. |
| `description` | body | `string` | no | Account description. |
| `id` | path | `string` | yes | Account ID. |
| `name` | body | `string` | yes | Account name. |
