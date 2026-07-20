# List Surveys with SurveySparrow

Retrieves all surveys from SurveySparrow.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [List Surveys](https://developers.surveysparrow.com/rest-apis/get-v-3-surveys/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_type` | query | `list` | no | Filter surveys by survey type. Accepted values: `0`, `1`, `10`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `archived` | query | `boolean` | no | Include archived or active surveys. |
| `survey_folder_id` | query | `string` | no | Filter surveys by the containing survey folder. |
| `created_date.gte` | query | `date` | no | Return surveys created on or after this date. |
| `created_date.lte` | query | `date` | no | Return surveys created on or before this date. |
| `updated_date.gte` | query | `date` | no | Return surveys updated on or after this date. |
| `updated_date.lte` | query | `date` | no | Return surveys updated on or before this date. |
