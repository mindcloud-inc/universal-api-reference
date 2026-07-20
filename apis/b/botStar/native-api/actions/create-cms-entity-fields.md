# Create CMS Entity Fields with BotStar

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/:botId/cms_entities/:entityId/fields`
- **Base URL:** `https://apis.botstar.com/v1`
- **Official documentation:** [Create CMS Entity Fields](https://apis.botstar.com/docs/#/CMS%20Entity%20Fields/post_bots__botId__cms_entities__entityId__fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | — |
| `entityId` | path | `string` | yes | — |
| `env` | query | `string` | no | — |
| `fields[]` | body | `array<object>` | yes | Array of CMS field objects to create. |
