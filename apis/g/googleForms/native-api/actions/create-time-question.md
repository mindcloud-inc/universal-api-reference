# Create Time Question with Google Forms

Creates a time question in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:batchUpdate`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Create Time Question](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `title` | body | `string` | yes | Question text shown to respondents. |
| `description` | body | `string` | no | Optional help text displayed below the question title. |
| `locationIndex` | body | `number` | yes | Where to place the new item in the form. |
| `required` | body | `boolean` | no | Require respondents to answer this question. |
| `duration` | body | `boolean` | no | Ask respondents for elapsed time instead of clock time. |
