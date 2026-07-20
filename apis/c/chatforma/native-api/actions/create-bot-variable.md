# Create Bot Variable with Chatforma

Creates a new bot variable in Chatforma.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/:botId/variables`
- **Base URL:** `https://api.pro.chatforma.com/public/v1`
- **Official documentation:** [Create Bot Variable](https://docs.chatforma.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `number` | yes | Bot ID that owns the variable |
| `type` | body | `string` | yes | Variable type |
| `name` | body | `string` | yes | Variable name |
