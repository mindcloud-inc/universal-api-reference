# List Survey Tracking Links with SmartSurvey

Retrieves tracking links for a SmartSurvey survey.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/{surveyId}/links`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [List Survey Tracking Links](https://docs.smartsurvey.io/reference/get_surveys-surveyid-links)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id whose links you are querying |
