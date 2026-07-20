# Create Interaction Response with Discord

Creates an interaction response in Discord.

## Endpoint

- **Method:** `POST`
- **Path:** `/interactions/:interactionId/:interactionToken/callback`
- **Base URL:** `https://discord.com/api/v10`
- **Official documentation:** [Create Interaction Response](https://docs.discord.com/developers/interactions/receiving-and-responding#create-interaction-response)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `interactionId` | path | `string` | yes | Interaction ID |
| `interactionToken` | path | `string` | yes | Interaction token |
| `with_response` | query | `boolean` | no | Return interaction callback response body |
| `type` | body | `number` | yes | Interaction callback type |
| `data` | body | `object` | no | Interaction callback data object |
