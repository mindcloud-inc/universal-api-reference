# Get Sent SMS with Notifyre SMS

Retrieves a sent SMS message from Notifyre.

## Endpoint

- **Method:** `GET`
- **Path:** `/sms/send/:messageId`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [Get Sent SMS](https://docs.notifyre.com/api/sms-sent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | Sent message identifier. |
