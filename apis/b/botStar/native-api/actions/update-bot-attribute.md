# Update Bot Attribute with BotStar

## Endpoint

- **Method:** `PATCH`
- **Path:** `/bots/:botId/attributes/:attributeId`
- **Base URL:** `https://apis.botstar.com/v1`
- **Official documentation:** [Update Bot Attribute](https://apis.botstar.com/docs/#/Bots/patch_bots__botId__attributes__attributeId_)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `attributeId` | path | `string` | yes |
| `botId` | path | `string` | yes |
| `desc` | body | `string` | no |
| `env` | query | `string` | no |
| `value` | body | `string` | no |
