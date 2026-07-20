# Set Collect Email with Google Forms

Updates a form's email collection settings in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:batchUpdate`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Set Collect Email](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `emailCollectionType` | body | `list` | yes | Whether and how the form collects respondent email addresses. Accepted values: `0`, `1`, `2`. |
