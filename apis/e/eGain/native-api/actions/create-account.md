# Create Account with eGain

Creates a new account in eGain.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts`
- **Base URL:** `https://api.ai.egain.cloud/conversation/conversationmgr/v3`
- **Official documentation:** [Create Account](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/account/createaccount.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | yes | Whether the account is active. |
| `address` | body | `string` | yes | Account address or identifier. |
| `channel.id` | body | `string` | yes | Channel ID. |
| `chatConfigurations.defaultLanguage` | body | `string` | no | Default language. |
| `chatConfigurations.entryPoint.id` | body | `string` | yes | Entry point ID. |
| `chatConfigurations.orchestration.id` | body | `string` | yes | Orchestration ID. |
| `chatConfigurations.timeout` | body | `number` | yes | Conversation timeout in minutes. |
| `description` | body | `string` | no | Account description. |
| `name` | body | `string` | yes | Account name. |
