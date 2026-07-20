# Update Channel with eGain

Updates an existing channel in eGain.

## Endpoint

- **Method:** `PUT`
- **Path:** `/channels/:id`
- **Base URL:** `https://api.ai.egain.cloud/conversation/conversationmgr/v3`
- **Official documentation:** [Update Channel](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/channel/updatechannel.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | yes | Whether channel is active. |
| `description` | body | `string` | yes | Channel description. |
| `displayName` | body | `string` | yes | Channel display name. |
| `icon` | body | `string` | yes | Channel icon. |
| `id` | path | `string` | yes | Channel ID. |
| `restrictions.inbound.maxTextLength` | body | `number` | yes | Inbound max text length. |
| `restrictions.outbound.maxTextLength` | body | `number` | yes | Outbound max text length. |
| `restrictions.outbound.midChatAuth` | body | `boolean` | yes | Whether mid chat auth is enabled. |
| `restrictions.outbound.systemMessages` | body | `boolean` | yes | Whether system messages are enabled. |
| `type` | body | `string` | yes | Channel type. |
