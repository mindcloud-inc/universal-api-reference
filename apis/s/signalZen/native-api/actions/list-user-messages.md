# List User Messages with SignalZen

Retrieves a user's messages from SignalZen.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/{userId}/messages`
- **Base URL:** `https://api.signalzen.com/external`
- **Official documentation:** [List User Messages](https://docs.signalzen.com/docs/api/messages/#get-all-messages-that-belong-to-a-user)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `number` | yes | The ID of the user whose messages you want to list. |
