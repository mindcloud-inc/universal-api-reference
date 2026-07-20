# Create Rating Question with Google Forms

Creates a rating question in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:batchUpdate`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Create Rating Question](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `title` | body | `string` | yes | Question title shown to respondents. |
| `description` | body | `string` | no | Optional help text shown under the title. |
| `locationIndex` | body | `number` | yes | Index where the question should be inserted. |
| `required` | body | `boolean` | no | Whether respondents must answer this question. |
| `ratingScaleLevel` | body | `number` | yes | Number of rating icons to show. |
| `iconType` | body | `list` | yes | Icon used for the rating scale. |
| `includeFormInResponse` | body | `boolean` | no | Return the updated form in the response. |
| `requiredRevisionId` | body | `string` | no | Only apply the update if the form is still at this revision. |
| `targetRevisionId` | body | `string` | no | Apply this update against a recent revision and let Google transform non-conflicting changes. |
