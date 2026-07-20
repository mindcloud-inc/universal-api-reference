# Export Translation with SurveySparrow

Retrieves a translation Excel file from SurveySparrow.

## Endpoint

- **Method:** `GET`
- **Path:** `/translation/export`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [Export Translation](https://developers.surveysparrow.com/rest-apis/get-v-3-translation-export/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | query | `number` | yes | Survey ID |
| `language_code` | query | `string` | yes | Language code |
| `include_labels` | query | `boolean` | no | Include labels in export |
