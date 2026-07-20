# Reschedule Message with Sendible

## Endpoint

- **Method:** `POST`
- **Path:** `0.1/tw/messages/reschedule`
- **Base URL:** `https://api.sendible.com`
- **Official documentation:** [Reschedule Message](https://support.sendible.com/hc/en-us)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | The message ID to reschedule. |
| `newSendDate` | body | `string` | yes | New message send datetime. |
| `recursUntil` | body | `string` | no | Optional recurrence end datetime. |
