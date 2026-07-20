# Get Private Chat Room URL with Morningmate

Retrieves a private chat room URL from Morningmate.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/chats/urls`
- **Base URL:** `https://api.morningmate.com`
- **Official documentation:** [Get Private Chat Room URL](https://api.morningmate.com/docs/api/v1/chats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `registerId` | query | `string` | yes | Morningmate author user ID |
| `receiverId` | query | `string` | yes | Morningmate receiver user ID |
