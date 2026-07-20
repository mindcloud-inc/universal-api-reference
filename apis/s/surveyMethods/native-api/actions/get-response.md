# Get Response with SurveyMethods

## Endpoint

- **Method:** `GET`
- **Path:** `/:loginId/:apiKey/responses/:surveyCode/detail/:responseCode/`
- **Base URL:** `https://api.surveymethods.com/v1`
- **Official documentation:** [Get Response](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyCode` | path | `string` | yes | SurveyMethods survey code. |
| `responseCode` | path | `string` | yes | SurveyMethods response code. |
