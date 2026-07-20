# Add Questions To Form with Google Forms

Adds multiple questions to a form in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:batchUpdate`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Add Questions To Form](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier returned by Create Form. |
| `questions[]` | body | `array<object>` | yes | Questions to add. Common fields per question: title, type (text, paragraph, choice, checkbox, dropdown, scale, date, time, rating), description, required, options, low, high, lowLabel, highLabel, includeTime, includeYear, duration, ratingScaleLevel, iconType. Advanced quiz fields: pointValue, correctAnswers. Send multiple values as a array. |
| `startIndex` | body | `number` | no | Index for the first inserted question. Later questions are inserted after it in order. |
| `includeFormInResponse` | body | `boolean` | no | Return the updated form in the response. |
| `requiredRevisionId` | body | `string` | no | Only apply the update if the form is still at this revision. |
| `targetRevisionId` | body | `string` | no | Apply this update against a recent revision and let Google transform non-conflicting changes. |
