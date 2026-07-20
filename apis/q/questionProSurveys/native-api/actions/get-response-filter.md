# Get Response Filter with QuestionPro Surveys

## Endpoint

- **Method:** `GET`
- **Path:** `surveys/:surveyId/responses/filter`
- **Base URL:** `https://api.questionpro.com/a/api/v2`
- **Official documentation:** [Get Response Filter](https://www.questionpro.com/api/get-responses-filter.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | QuestionPro survey ID. |
| `extRef` | query | `string` | no | Filter responses by external reference. |
| `custom1` | query | `string` | no | Filter responses by custom1. |
| `custom2` | query | `string` | no | Filter responses by custom2. |
| `custom3` | query | `string` | no | Filter responses by custom3. |
| `custom4` | query | `string` | no | Filter responses by custom4. |
| `custom5` | query | `string` | no | Filter responses by custom5. |
| `page` | query | `number` | no | Page number. |
| `perPage` | query | `number` | no | Results per page. |
