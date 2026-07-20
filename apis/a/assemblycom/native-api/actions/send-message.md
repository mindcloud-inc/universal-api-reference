# Send Message with Assembly.com

Sends a message in an Assembly.com message channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages`
- **Base URL:** `https://api.assembly.com/v1`
- **Official documentation:** [Send Message](https://docs.assembly.com/reference/send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The contents of the message. |
| `channelId` | body | `string` | yes | The Message Channel where the message will be sent. |
| `senderId` | body | `string` | no | Send this message on behalf of a channel member. |
