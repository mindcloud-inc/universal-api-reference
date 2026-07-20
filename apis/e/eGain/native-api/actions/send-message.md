# Send Message with eGain

Sends conversation messages in eGain Conversation Hub.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/messages`
- **Base URL:** `https://api.ai.egain.cloud/conversation/conversationmgr/v3`
- **Official documentation:** [Send Message](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/conversation/sendmessage.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages.message[0].content` | body | `string` | no | Raw message content object. |
| `messages.message[0].content.text` | body | `string` | yes | Text message content. |
| `messages.message[0].conversation.account.address` | body | `string` | yes | Conversation account address. |
| `messages.message[0].conversation.account.channel.type` | body | `string` | yes | Channel type for the conversation account. |
| `messages.message[0].conversation.customer.contacts.contact[0].address` | body | `string` | yes | Customer contact address. |
| `messages.message[0].conversation.customer.contacts.contact[0].type` | body | `string` | yes | Customer contact type. |
| `messages.message[0].conversation.entryPoint.id` | body | `string` | yes | Entry point ID for the conversation. |
| `messages.message[0].sender.type` | body | `string` | yes | Sender client type. |
| `messages.message[0].type.value` | body | `string` | yes | Message type value. |
