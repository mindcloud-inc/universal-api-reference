# Get Response Question with SurveyMethods

## Endpoint

- **Method:** `GET`
- **Path:** `/:loginId/:apiKey/responses/:surveyCode/detail/:responseCode/:questionCode/`
- **Base URL:** `https://api.surveymethods.com/v1`
- **Official documentation:** [Get Response Question](https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyCode` | path | `string` | yes | SurveyMethods survey code. |
| `responseCode` | path | `string` | yes | SurveyMethods response code. |
| `questionCode` | path | `string` | yes | SurveyMethods question code. |
