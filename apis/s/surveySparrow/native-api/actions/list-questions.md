# List Questions with SurveySparrow

Retrieves survey questions from SurveySparrow.

## Endpoint

- **Method:** `GET`
- **Path:** `/questions`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [List Questions](https://developers.surveysparrow.com/rest-apis/get-v-3-questions/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | query | `number` | yes | ID of the survey. |
| `tag_name` | query | `string` | no | Filter questions by tag name. |
| `language_label` | query | `string` | no | Filter questions by language label. |
