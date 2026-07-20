# Create Conversation with Rocketlane

Creates a conversation in Rocketlane.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.0/conversations`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [Create Conversation](https://developer.rocketlane.com/reference/create-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeFields` | query | `list<string>` | no | Use this query parameter to opt in for fields to be returned in the response body. Use comma separated values to fetch the respective fields. If left blank, default properties are returned. |
| `includeAllFields` | query | `boolean` | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
| `name` | body | `string` | yes | Conversation name |
| `description` | body | `string` | no | Conversation description |
| `source` | body | `object` | yes | Source associated with the conversation |
| `allMembers` | body | `boolean` | no | Conversation all members inclusion |
| `members` | body | `list<object>` | no | Conversation members |
| `private` | body | `boolean` | no | Conversation privacy |
