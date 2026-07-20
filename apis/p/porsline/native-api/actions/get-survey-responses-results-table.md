# Get Survey Responses Results Table with Porsline

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/surveys/:survey_id/responses/results-table/`
- **Base URL:** `https://survey.porsline.com`
- **Official documentation:** [Get Survey Responses Results Table](https://developers.porsline.com/#tag/Results/paths/~1api~1v2~1surveys~1{survey_id}~1responses~1results-table~1/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | path | `number` | yes | The id of the target survey. |
| `since` | query | `string` | no | Limit submitted responders since the specified ISO 8601 datetime. |
| `until` | query | `string` | no | Limit submitted responders until the specified ISO 8601 datetime. |
| `sort` | query | `string` | no | Sort criteria in the Porsline {col_type},{object_id},{asc\|desc} format. |
| `page` | query | `number` | no | Page number. |
| `page_size` | query | `number` | no | Maximum number of responders to return. |
