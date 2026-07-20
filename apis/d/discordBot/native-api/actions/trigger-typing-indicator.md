# Trigger Typing Indicator with Discord-Bot

Triggers a typing indicator in a Discord channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/channels/:channelId/typing`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Trigger Typing Indicator](https://docs.discord.com/developers/resources/channel#trigger-typing-indicator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | Discord channel ID. |
