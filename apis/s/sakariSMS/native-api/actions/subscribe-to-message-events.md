# Subscribe To Message Events with Sakari SMS

Subscribes to message events in Sakari SMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/:accountId/webhooks`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [Subscribe To Message Events](https://developer.sakari.io/api-reference/webhooks/subscribe-to-message-events)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `url` | body | `string` | yes |
| `eventTypes[]` | body | `array<string>` | no |
