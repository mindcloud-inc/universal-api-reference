# Delete Bot with Botsonic

Deletes an existing bot from Botsonic.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/business/bot/:botId`
- **Base URL:** `https://api.botsonic.ai`
- **Official documentation:** [Delete Bot](https://docs.botsonic.com/reference/delete_bot_v1_business_bot__bot_id__delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_id` | path | `string` | yes | bot_id of the bot to delete. |
| `workspace_id` | query | `string` | no | Optional workspace identifier. |
