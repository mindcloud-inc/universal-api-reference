# Get User Variable with Chatforma

Retrieves user variable details from Chatforma.

## Endpoint

- **Method:** `GET`
- **Path:** `/bots/:botId/variables/:variableId/user/:botUserId`
- **Base URL:** `https://api.pro.chatforma.com/public/v1`
- **Official documentation:** [Get User Variable](https://docs.chatforma.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `number` | yes | Bot ID that owns the variable |
| `variableId` | path | `number` | yes | Variable ID to fetch for a user |
| `botUserId` | path | `number` | yes | Bot user ID to fetch the variable for |
