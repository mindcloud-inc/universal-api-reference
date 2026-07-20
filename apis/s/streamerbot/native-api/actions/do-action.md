# Do Action with Streamer.bot

Triggers an existing action in Streamer.bot.

## Endpoint

- **Method:** `POST`
- **Path:** `/DoAction`
- **Base URL:** `https://allow-freely-princess-carefully.trycloudflare.com`
- **Official documentation:** [Do Action](https://docs.streamer.bot/api/http/requests/do-action)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action.id` | body | `string` | no | GUID of the Streamer.bot action to execute. |
| `action.name` | body | `string` | no | Name of the Streamer.bot action to execute. |
| `args` | body | `object` | no | Optional key-value arguments to pass through to the Streamer.bot action. |
