# List CMS Entity Items with BotStar

## Endpoint

- **Method:** `GET`
- **Path:** `/bots/:botId/cms_entities/:entityId/items`
- **Base URL:** `https://apis.botstar.com/v1`
- **Official documentation:** [List CMS Entity Items](https://apis.botstar.com/docs/#/CMS%20Entity%20Items/get_bots__botId__cms_entities__entityId__items)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `botId` | path | `string` | yes |
| `entityId` | path | `string` | yes |
| `env` | query | `string` | no |
| `page` | query | `number` | no |
| `limit` | query | `number` | no |
| `name` | query | `string` | no |
| `status` | query | `string` | no |
