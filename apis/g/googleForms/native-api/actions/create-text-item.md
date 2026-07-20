# Create Text Item with Google Forms

Creates a static text item in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:batchUpdate`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Create Text Item](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `title` | body | `string` | no | Text block title. |
| `description` | body | `string` | no | Text block body or supporting description. |
| `locationIndex` | body | `number` | yes | Index where the text block should be inserted. |
| `includeFormInResponse` | body | `boolean` | no | Return the updated form in the response. |
| `requiredRevisionId` | body | `string` | no | Only apply the update if the form is still at this revision. |
| `targetRevisionId` | body | `string` | no | Apply this update against a recent revision and let Google transform non-conflicting changes. |
