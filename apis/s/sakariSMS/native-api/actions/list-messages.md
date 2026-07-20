# List Messages with Sakari SMS

Retrieves account messages from Sakari SMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/accounts/:accountId/messages`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [List Messages](https://developer.sakari.io/api-reference/messages/fetch-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | query | `string` | no | ID of contact |
| `conversationId` | query | `string` | no | ID of conversation |
