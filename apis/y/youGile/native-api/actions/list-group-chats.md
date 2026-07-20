# List group chats with YouGile

Retrieves a list of group chats from YouGile.

## Endpoint

- **Method:** `GET`
- **Path:** `/group-chats`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [List group chats](https://ru.yougile.com/api-v2#/operations/GroupChatController_search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeDeleted` | query | `boolean` | no | Include deleted group chats in the result. |
| `title` | query | `string` | no | Filter group chats by title. |
