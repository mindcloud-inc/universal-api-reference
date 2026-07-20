# Create CMS Entity with BotStar

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/:botId/cms_entities`
- **Base URL:** `https://apis.botstar.com/v1`
- **Official documentation:** [Create CMS Entity](https://apis.botstar.com/docs/#/CMS%20Entities/post_bots__botId__cms_entities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | — |
| `env` | query | `string` | no | — |
| `name` | body | `string` | yes | — |
| `fields[]` | body | `array<object>` | no | Optional array of CMS field objects to create with the entity. |
