# List Media with Framework360

## Endpoint

- **Method:** `GET`
- **Path:** `media/list`
- **Base URL:** `https://mindcloudstage0.framework360.site/m/api`
- **Official documentation:** [List Media](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `directory` | query | `string` | no | Media directory to list. |
| `page` | query | `number` | no | Results page number. |
| `limit` | query | `number` | no | Maximum number of media items per page. |
| `query` | query | `string` | no | Free-text search term. |
| `global` | query | `boolean` | no | Whether to include global media. |
