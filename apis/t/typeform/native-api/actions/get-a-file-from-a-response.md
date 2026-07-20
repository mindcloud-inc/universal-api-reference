# Get a File from a Response with Typeform

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId/responses/:responseId/fields/:fieldId/files/:filename`
- **Base URL:** `https://api.typeform.com`
- **Official documentation:** [Get a File from a Response](https://www.typeform.com/developers/responses/reference/get-a-file-from-a-response/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fieldId` | path | `string` | yes | Typeform field identifier. |
| `filename` | path | `string` | yes | Uploaded file name. |
| `formId` | path | `string` | yes | Typeform form identifier. |
| `inline` | query | `boolean` | no | Return file inline instead of attachment. |
| `responseId` | path | `string` | yes | Typeform response identifier. |
