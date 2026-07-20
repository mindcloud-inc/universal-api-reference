# Search Chats with Instabot

Finds chats in Instabot by search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/instabot/chats/search`
- **Base URL:** `https://api.instabot.io/v1`
- **Official documentation:** [Search Chats](https://docs.instabot.io/reference/post_instabot-chats-search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchString` | body | `string` | no | Text used to search chats. |
| `startDate` | body | `date` | no | Start of the chat search date window. |
| `endDate` | body | `date` | no | End of the chat search date window. |
| `botDeletionStatus` | body | `string` | no | Filter chats by bot deletion status. |
