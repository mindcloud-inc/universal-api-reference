# Update Form Item with Google Forms

Updates an existing form item in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:batchUpdate`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Update Form Item](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `title` | body | `string` | no | New item title. If update mask is omitted, this adds title to the mask automatically. |
| `description` | body | `string` | no | New item description. If update mask is omitted, this adds description to the mask automatically. |
| `required` | body | `boolean` | no | For question items, whether respondents must answer the question. |
| `item` | body | `object` | no | Advanced: full Google Forms Item object with replacement values. Use when common fields are not enough. |
| `locationIndex` | body | `number` | yes | Index of the item to update. |
| `updateMask` | body | `string` | no | Advanced: comma-separated item fields to update. Defaults from provided common fields when omitted. |
| `includeFormInResponse` | body | `boolean` | no | Return the updated form in the response. |
| `requiredRevisionId` | body | `string` | no | Only apply the update if the form is still at this revision. |
| `targetRevisionId` | body | `string` | no | Apply this update against a recent revision and let Google transform non-conflicting changes. |
