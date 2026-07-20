# Create Date Question with Google Forms

Creates a date question in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:batchUpdate`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Create Date Question](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `title` | body | `string` | yes | Question text shown to respondents. |
| `description` | body | `string` | no | Optional help text displayed below the question title. |
| `locationIndex` | body | `number` | yes | Where to place the new item in the form. |
| `required` | body | `boolean` | no | Require respondents to answer this question. |
| `includeTime` | body | `boolean` | no | Allow respondents to include a time with the date. |
| `includeYear` | body | `boolean` | no | Ask respondents for a year with the date. |
