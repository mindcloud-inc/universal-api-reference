# Create Channel with eGain

Creates a new channel in eGain.

## Endpoint

- **Method:** `POST`
- **Path:** `/channels`
- **Base URL:** `https://api.ai.egain.cloud/conversation/conversationmgr/v3`
- **Official documentation:** [Create Channel](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/channel/createchannel.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | yes | Whether the channel is active. |
| `description` | body | `string` | yes | Channel description. |
| `displayName` | body | `string` | yes | Channel display name. |
| `icon` | body | `string` | yes | Base64 icon data. |
| `restrictions.inbound.maxTextLength` | body | `number` | yes | Maximum inbound text length. |
| `restrictions.outbound.maxTextLength` | body | `number` | yes | Maximum outbound text length. |
| `restrictions.outbound.midChatAuth` | body | `boolean` | yes | Whether mid-chat auth is enabled. |
| `restrictions.outbound.systemMessages` | body | `boolean` | yes | Whether outbound system messages are enabled. |
| `type` | body | `string` | yes | Channel type. |
