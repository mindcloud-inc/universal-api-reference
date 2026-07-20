# Delete Bot Variable with Chatforma

Deletes an existing bot variable from Chatforma.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/bots/:botId/variables/:variableId`
- **Base URL:** `https://api.pro.chatforma.com/public/v1`
- **Official documentation:** [Delete Bot Variable](https://docs.chatforma.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `number` | yes | Bot ID that owns the variable |
| `variableId` | path | `number` | yes | Variable ID to delete |
