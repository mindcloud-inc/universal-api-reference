# Get Message by ID with Sakari SMS

Retrieves a message from Sakari SMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/accounts/:accountId/messages/:messageId`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [Get Message by ID](https://developer.sakari.io/api-reference/messages/fetch-message-by-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `messageId` | path | `string` | yes |
