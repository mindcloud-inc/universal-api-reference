# Create Question Group Item with Google Forms

Creates a question group item in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:batchUpdate`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Create Question Group Item](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `title` | body | `string` | yes | Question group title. |
| `description` | body | `string` | no | Optional help text displayed below the group title. |
| `locationIndex` | body | `number` | yes | Where to place the new question group in the form. |
| `rows[]` | body | `array<string>` | yes | Row question labels. Send multiple values as a array. |
| `columns[]` | body | `array<string>` | yes | Shared choice labels for each row. Send multiple values as a array. |
| `choiceType` | body | `list` | yes | Grid choice type. Google supports radio or checkbox for grids. Accepted values: `0`, `1`. |
| `shuffleQuestions` | body | `boolean` | no | Randomize row order for respondents. |
