# List Webhooks By Channel with 2Chat

Retrieves webhook subscriptions for a 2Chat channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks/channel/:channel_uuid`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [List Webhooks By Channel](https://developers.2chat.co/docs/API/Webhooks/list-webhooks-by-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_uuid` | path | `string` | yes | The UUID of the channel to list webhook subscriptions for. |
