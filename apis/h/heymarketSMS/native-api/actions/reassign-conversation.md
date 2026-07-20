# Reassign Conversation with Heymarket SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/conversations/reassign`
- **Base URL:** `https://api.heymarket.com`
- **Official documentation:** [Reassign Conversation](https://heymarket.docs.apiary.io/api-description-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | body | `number` | yes | Unique identifier of the inbox. |
| `user_id` | body | `number` | yes | Unique identifier of the current user. |
| `reassign_id` | body | `number` | yes | Unique identifier of the user to assign the conversation to. |
| `target` | body | `string` | no | Phone number for the conversation. |
| `targets[]` | body | `array<string>` | no | Phone numbers for a group MMS conversation. |
