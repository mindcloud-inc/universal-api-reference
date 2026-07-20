# Get Conversation with Rocketlane

Retrieves a conversation from Rocketlane.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.0/conversations/:conversationId`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [Get Conversation](https://developer.rocketlane.com/reference/get-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `number` | yes | The ID of the conversation object |
| `includeFields` | query | `list<string>` | no | This query parameter allows you to specify which fields should be returned in the response body by selecting from the drop down. To get the relevant fields, use comma separated values. If the field is left blank, the default properties are returned. |
| `includeAllFields` | query | `boolean` | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
