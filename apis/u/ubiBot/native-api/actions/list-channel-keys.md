# List Channel Keys with UbiBot

Retrieves channel API keys from UbiBot.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/:channelId/api_keys`
- **Base URL:** `https://webapi.ubibot.com`
- **Official documentation:** [List Channel Keys](https://www.ubibot.com/platform-api/1181/list-channel-api-keys/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | no | UbiBot channel identifier from the channel URL or channel list. |
