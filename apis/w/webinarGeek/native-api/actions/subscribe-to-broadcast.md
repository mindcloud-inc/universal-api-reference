# Subscribe to Broadcast with WebinarGeek

## Endpoint

- **Method:** `POST`
- **Path:** `/broadcasts/:broadcastId/subscriptions`
- **Base URL:** `https://app.webinargeek.com/api/v2`
- **Official documentation:** [Subscribe to Broadcast](https://static.webinargeek.com/api-documentation.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcastId` | path | `number` | yes | ID of the broadcast to subscribe the viewer to |
| `firstname` | body | `string` | yes | First name of the subscribing user |
| `email` | body | `string` | yes | Email address of the subscribing user |
