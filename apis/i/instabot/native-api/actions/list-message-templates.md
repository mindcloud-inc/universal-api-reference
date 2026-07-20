# List Message Templates with Instabot

Retrieves message templates from Instabot.

## Endpoint

- **Method:** `GET`
- **Path:** `/instabot/messageTemplates`
- **Base URL:** `https://api.instabot.io/v1`
- **Official documentation:** [List Message Templates](https://docs.instabot.io/reference/get_instabot-messagetemplates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isActive` | query | `boolean` | no | Filter message templates by active state. |
| `name` | query | `string` | no | Filter message templates by name. |
| `text` | query | `string` | no | Filter message templates by text. |
