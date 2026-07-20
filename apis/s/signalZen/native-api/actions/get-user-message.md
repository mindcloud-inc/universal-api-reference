# Get User Message with SignalZen

Retrieves a user's message from SignalZen.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/{userId}/messages/{messageId}`
- **Base URL:** `https://api.signalzen.com/external`
- **Official documentation:** [Get User Message](https://docs.signalzen.com/docs/api/messages/#get-a-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `number` | yes | The ID of the user who owns the message. |
| `messageId` | path | `number` | yes | The ID of the message to retrieve. |
