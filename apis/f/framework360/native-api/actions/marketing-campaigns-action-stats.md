# List Campaign Action Stats with Framework360

## Endpoint

- **Method:** `GET`
- **Path:** `marketing/campaigns/action/stats`
- **Base URL:** `https://mindcloudstage0.framework360.site/m/api`
- **Official documentation:** [List Campaign Action Stats](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | query | `string` | yes | Marketing campaign ID. |
| `type` | query | `string` | yes | Campaign action type. |
| `id` | query | `string` | yes | Campaign action ID. |
| `page` | query | `number` | no | Results page number. |
| `limit` | query | `number` | no | Maximum number of results per page. |
