# Update Form Settings with Google Forms

Updates a form's settings in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:batchUpdate`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Update Form Settings](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `isQuiz` | body | `boolean` | no | Whether the form is a quiz. |
| `emailCollectionType` | body | `list` | no | Whether and how the form collects respondent email addresses. Accepted values: `0`, `1`, `2`. |
| `updateMask` | body | `string` | no | Comma-separated FormSettings fields such as quizSettings.isQuiz,emailCollectionType. Defaults from provided fields when omitted. |
