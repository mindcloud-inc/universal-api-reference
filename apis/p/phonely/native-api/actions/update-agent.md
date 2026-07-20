# Update Agent with Phonely

Updates an agent in Phonely.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/update-agent`
- **Base URL:** `https://app.phonely.ai`
- **Official documentation:** [Update Agent](https://docs.phonely.ai/api-reference/endpoint/update-agent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | body | `string` | yes | Your Phonely user ID. |
| `agentId` | body | `string` | yes | The ID of the agent to update. |
| `agentName` | body | `string` | no | New name for the agent. Maximum 50 characters. Maximum length: 50. |
| `greetingMessage` | body | `string` | no | New greeting message. Maximum 500 characters. Maximum length: 500. |
| `conversationStyle` | body | `string` | no | Conversation style. Use one of: Casual, Humorous, Direct, Formal, Persuasive, Friendly. |
| `humanizeConversation` | body | `boolean` | no | Whether to humanize the conversation. |
| `voiceId` | body | `string` | no | ID of the voice to use for the agent. |
| `orgId` | body | `string` | no | Organization ID to move the agent to. |
