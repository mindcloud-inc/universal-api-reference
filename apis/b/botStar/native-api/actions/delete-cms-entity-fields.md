# Delete CMS Entity Fields with BotStar

## Endpoint

- **Method:** `DELETE`
- **Path:** `/bots/:botId/cms_entities/:entityId/fields`
- **Base URL:** `https://apis.botstar.com/v1`
- **Official documentation:** [Delete CMS Entity Fields](https://apis.botstar.com/docs/#/CMS%20Entity%20Fields/delete_bots__botId__cms_entities__entityId__fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | — |
| `entityId` | path | `string` | yes | — |
| `env` | query | `string` | no | — |
| `unique_names` | query | `string` | no | Comma-separated entity field unique_name values to delete. |
