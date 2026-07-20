# Update CMS Entity with BotStar

## Endpoint

- **Method:** `PATCH`
- **Path:** `/bots/:botId/cms_entities/:entityId`
- **Base URL:** `https://apis.botstar.com/v1`
- **Official documentation:** [Update CMS Entity](https://apis.botstar.com/docs/#/CMS%20Entities/patch_bots__botId__cms_entities__entityId_)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `botId` | path | `string` | yes |
| `entityId` | path | `string` | yes |
| `env` | query | `string` | no |
| `name` | body | `string` | no |
