# Add Conversation Members with Rocketlane

Adds members to a conversation in Rocketlane.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.0/conversations/:conversationId/add-members`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [Add Conversation Members](https://developer.rocketlane.com/reference/add-members-to-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `number` | yes | The ID of the conversation object |
| `includeFields` | query | `list<string>` | no | Use this query parameter to opt in for fields to be returned in the response body. Use comma separated values to fetch the respective fields. If left blank, default properties are returned. |
| `includeAllFields` | query | `boolean` | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
