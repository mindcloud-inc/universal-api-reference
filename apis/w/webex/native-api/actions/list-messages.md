# List Messages with Webex

Lists messages in your Webex account.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages`
- **Base URL:** `https://webexapis.com/v1`
- **Official documentation:** [List Messages](https://developer.webex.com/messaging/docs/api/v1/messages/list-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `max` | query | `number` | no | Maximum number of messages to return. |
| `roomId` | query | `string` | no | Filter messages to one room. |
