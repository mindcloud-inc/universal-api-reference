# List Survey Responses with SmartSurvey

Retrieves survey responses from a SmartSurvey survey.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/{surveyId}/responses`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [List Survey Responses](https://docs.smartsurvey.io/reference/get_surveys-surveyid-responses)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id whose Responses you are querying |
| `completed` | query | `number` | no | Whether to only include completed responses |
| `translation_id` | query | `number` | no | The translation for the results - defaults to English |
| `since` | query | `number` | no | Unix timestamp to filter results after a date/time |
| `until` | query | `number` | no | Unix timestamp to filter results before a date/time |
| `filter_id` | query | `number` | no | Optional filter id for the results |
| `tracking_link_id` | query | `number` | no | Tracking link id to filter results |
| `unique_id` | query | `string` | no | Filter on the user unique id |
| `include_labels` | query | `boolean` | no | Whether to include question and page labels (reduces the size of the response) |
