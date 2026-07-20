# Get Bot API Key with Botsonic

Retrieves a bot API key from Botsonic.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/business/bot/:botId/bot-api-key`
- **Base URL:** `https://api.botsonic.ai`
- **Official documentation:** [Get Bot API Key](https://docs.botsonic.com/reference/get_bot_api_key_v1_business_bot__bot_id__bot_api_key_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_id` | path | `string` | yes | bot_id of the bot. |
| `workspace_id` | query | `string` | no | Optional workspace identifier. |
