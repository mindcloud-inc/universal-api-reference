# Get Survey Responses Export with Porsline

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/surveys/:survey_id/responses/export/`
- **Base URL:** `https://survey.porsline.com`
- **Official documentation:** [Get Survey Responses Export](https://developers.porsline.com/#tag/Results/paths/~1api~1v2~1surveys~1{survey_id}~1responses~1export~1/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | path | `number` | yes | The id of the target survey. |
| `export_format` | query | `string` | no | Export format. 1: xlsx, 2: csv. |
| `since` | query | `string` | no | Limit submitted responders since the specified ISO 8601 datetime. |
| `until` | query | `string` | no | Limit submitted responders until the specified ISO 8601 datetime. |
| `sort` | query | `string` | no | Sort criteria in the Porsline {col_type},{object_id},{asc\|desc} format. |
| `filter` | query | `number` | no | Filter ID to apply on results. |
| `inline_filter` | query | `string` | no | Inline filter expression in the Porsline documented format. |
