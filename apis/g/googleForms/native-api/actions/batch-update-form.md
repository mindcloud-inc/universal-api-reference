# Batch Update Form with Google Forms

Applies batch updates to a form in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:batchUpdate`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Batch Update Form](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `requests[]` | body | `array<object>` | yes | Raw Google Forms batchUpdate request objects. Use this for advanced updateFormInfo, updateSettings, createItem, moveItem, deleteItem, or updateItem calls. Send multiple values as a array. |
| `includeFormInResponse` | body | `boolean` | no | Return the updated form in the response. |
| `requiredRevisionId` | body | `string` | no | Strict write-control revision ID; request fails if it is not current. |
| `targetRevisionId` | body | `string` | no | Optimistic write-control revision ID; Google transforms against later edits when possible. |
