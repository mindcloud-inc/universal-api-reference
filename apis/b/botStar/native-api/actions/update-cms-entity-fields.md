# Update CMS Entity Fields with BotStar

## Endpoint

- **Method:** `PATCH`
- **Path:** `/bots/:botId/cms_entities/:entityId/fields`
- **Base URL:** `https://apis.botstar.com/v1`
- **Official documentation:** [Update CMS Entity Fields](https://apis.botstar.com/docs/#/CMS%20Entity%20Fields/patch_bots__botId__cms_entities__entityId__fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | — |
| `entityId` | path | `string` | yes | — |
| `env` | query | `string` | no | — |
| `fields[]` | body | `array<object>` | yes | Array of CMS field objects to update. |
