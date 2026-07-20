# Get Sent SMS Recipient with Notifyre SMS

Retrieves sent SMS recipient details from Notifyre.

## Endpoint

- **Method:** `GET`
- **Path:** `/sms/send/:messageId/recipients/:recipientId`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [Get Sent SMS Recipient](https://docs.notifyre.com/api/sms-sent-recipient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | Sent message identifier. |
| `recipientId` | path | `string` | yes | Recipient identifier on the sent message. |
