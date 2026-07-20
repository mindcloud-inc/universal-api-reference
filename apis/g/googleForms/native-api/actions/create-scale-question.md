# Create Scale Question with Google Forms

Creates a scale question in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:batchUpdate`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Create Scale Question](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `title` | body | `string` | yes | Question text shown to respondents. |
| `description` | body | `string` | no | Optional help text displayed below the question title. |
| `locationIndex` | body | `number` | yes | Where to place the new item in the form. |
| `required` | body | `boolean` | no | Require respondents to answer this question. |
| `low` | body | `number` | yes | Lowest number in the scale. |
| `high` | body | `number` | yes | Highest number in the scale. |
| `lowLabel` | body | `string` | no | Optional label for the low end of the scale. |
| `highLabel` | body | `string` | no | Optional label for the high end of the scale. |
