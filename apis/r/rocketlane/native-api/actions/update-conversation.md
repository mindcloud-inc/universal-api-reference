# Update Conversation with Rocketlane

Updates a conversation in Rocketlane.

## Endpoint

- **Method:** `PUT`
- **Path:** `/1.0/conversations/:conversationId`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [Update Conversation](https://developer.rocketlane.com/reference/update-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `number` | yes | The ID of the conversation object |
| `includeFields` | query | `list<string>` | no | Use this query parameter to opt in for fields to be returned in the response body. Use comma separated values to fetch the respective fields. If left blank, default properties are returned. |
| `includeAllFields` | query | `boolean` | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
| `conversationId` | body | `number` | no | Conversation ID |
| `name` | body | `string` | no | Conversation name |
| `description` | body | `string` | no | Conversation description |
| `allMembers` | body | `boolean` | no | Conversation all members inclusion |
