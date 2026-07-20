# Get Channel with UbiBot

Retrieves a channel and its latest sensor data from UbiBot.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/:channelId`
- **Base URL:** `https://webapi.ubibot.com`
- **Official documentation:** [Get Channel](https://www.ubibot.com/platform-api/1174/view-channel/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | UbiBot channel identifier from the channel URL or channel list. |
