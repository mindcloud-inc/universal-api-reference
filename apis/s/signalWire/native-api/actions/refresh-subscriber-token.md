# Refresh Subscriber Token with SignalWire

Refreshes a subscriber token in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/fabric/subscribers/tokens/refresh`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Refresh Subscriber Token](https://signalwire.com/docs/apis/rest/subscribers/tokens/refresh-subscriber-token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `refresh_token` | body | `string` | yes | The refresh token previously issued alongside a subscriber access token. This token is used to request a new access token. |
