# List Campaign Contacts with Framework360

## Endpoint

- **Method:** `GET`
- **Path:** `marketing/campaigns/contacts`
- **Base URL:** `https://mindcloudstage0.framework360.site/m/api`
- **Official documentation:** [List Campaign Contacts](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | query | `number` | yes | Marketing campaign ID. |
| `page` | query | `number` | no | Results page number. |
| `limit` | query | `number` | no | Maximum number of contacts per page. |
| `query` | query | `string` | no | Free-text contact filter. |
