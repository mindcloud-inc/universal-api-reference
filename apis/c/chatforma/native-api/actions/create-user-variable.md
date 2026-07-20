# Create User Variable with Chatforma

Creates a new user variable in Chatforma.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/:botId/variables/:variableId/user/:botUserId`
- **Base URL:** `https://api.pro.chatforma.com/public/v1`
- **Official documentation:** [Create User Variable](https://docs.chatforma.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `number` | yes | Bot ID that owns the variable |
| `variableId` | path | `number` | yes | Variable ID to set for a user |
| `botUserId` | path | `number` | yes | Bot user ID that receives the variable value |
| `value` | body | `string` | yes | Variable value to set |
