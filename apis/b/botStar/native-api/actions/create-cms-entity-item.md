# Create CMS Entity Item with BotStar

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/:botId/cms_entities/:entityId/items`
- **Base URL:** `https://apis.botstar.com/v1`
- **Official documentation:** [Create CMS Entity Item](https://apis.botstar.com/docs/#/CMS%20Entity%20Items/post_bots__botId__cms_entities__entityId__items)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `botId` | path | `string` | yes |
| `entityId` | path | `string` | yes |
| `env` | query | `string` | no |
| `name` | body | `string` | yes |
| `status` | body | `string` | no |
