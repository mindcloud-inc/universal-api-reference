# Create Conversation with Kommunicate

Creates a new conversation in Kommunicate.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/ws/group/conversation`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Create Conversation](https://docs.kommunicate.io/docs/api-detail#create-a-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupName` | body | `string` | yes | Conversation title. |
| `clientGroupId` | body | `number` | no | Optional client-generated conversation identifier. |
| `groupMemberList[]` | body | `array<string>` | yes | List of user, agent, or bot IDs to add to the conversation. |
| `metadata` | body | `object` | no | Optional conversation configuration flags and values. |
