# Create Conversation With Assignee with Kommunicate

Creates a new conversation with an assignee in Kommunicate.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/ws/group/conversation`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Create Conversation With Assignee](https://docs.kommunicate.io/docs/api-detail#create-a-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupName` | body | `string` | yes | Conversation title. |
| `groupMemberList[]` | body | `array<string>` | yes | List of user, agent, or bot IDs to add to the conversation. |
| `assignee` | body | `string` | yes | Agent or bot ID to force-assign when skip routing is enabled. |
| `clientGroupId` | body | `number` | no | Optional client-generated conversation identifier. |
