# Update Channel with Smart Sender

Updates a channel's activity status in Smart Sender.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/channels/:channelId`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [Update Channel](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444598/Channels%2BAPI%2B-%2Ben)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | The Smart Sender channel ID. |
| `state` | body | `boolean` | yes | Boolean activity status for the channel. |
