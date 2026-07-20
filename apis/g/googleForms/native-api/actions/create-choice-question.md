# Create Choice Question with Google Forms

Creates a choice question in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:batchUpdate`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Create Choice Question](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `title` | body | `string` | yes | Question text shown to respondents. |
| `description` | body | `string` | no | Optional help text displayed below the question title. |
| `locationIndex` | body | `number` | yes | Where to place the new item in the form. |
| `required` | body | `boolean` | no | Require respondents to answer this question. |
| `type` | body | `list` | yes | Choice question type: radio buttons, checkboxes, or dropdown. Accepted values: `0`, `1`, `2`. |
| `options[]` | body | `array<string>` | yes | Choices shown to respondents. Send multiple values as a array. |
| `shuffle` | body | `boolean` | no | Randomize options for each respondent. |
| `pointValue` | body | `number` | no | Quiz point value for this question. |
| `correctAnswers[]` | body | `array<string>` | no | Choice values that are correct for quiz grading. Send multiple values as a array. |
