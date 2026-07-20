# Update Form Info with Google Forms

Updates a form's title or description in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:batchUpdate`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Update Form Info](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `title` | body | `string` | no | New visible form title. Include this or Description. |
| `description` | body | `string` | no | New form description. Include this or Title. |
| `updateMask` | body | `string` | no | Comma-separated Info fields to update, such as title,description. Defaults from provided fields when omitted. |
| `includeFormInResponse` | body | `boolean` | no | Return the updated form in the response. |
| `targetRevisionId` | body | `string` | no | Optional optimistic write-control revision ID; Google will transform against later edits when possible. |
| `requiredRevisionId` | body | `string` | no | Optional strict write-control revision ID; request fails if it is not current. |
