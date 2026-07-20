# Get Bot with Botsonic

Retrieves a specific bot from Botsonic.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/business/bot/:botId`
- **Base URL:** `https://api.botsonic.ai`
- **Official documentation:** [Get Bot](https://docs.botsonic.com/reference/get_specific_bot_v1_business_bot__bot_id__get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_id` | path | `string` | yes | bot_id of the bot. |
| `workspace_id` | query | `string` | no | Optional workspace identifier. |
