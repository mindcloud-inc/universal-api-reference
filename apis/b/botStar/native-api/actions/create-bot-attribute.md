# Create Bot Attribute with BotStar

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/:botId/attributes`
- **Base URL:** `https://apis.botstar.com/v1`
- **Official documentation:** [Create Bot Attribute](https://apis.botstar.com/docs/#/Bots/post_bots__botId__attributes)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `botId` | path | `string` | yes |
| `data_type` | body | `string` | yes |
| `desc` | body | `string` | no |
| `env` | query | `string` | no |
| `name` | body | `string` | yes |
| `value` | body | `string` | no |
