# Delete Responses with Typeform

## Endpoint

- **Method:** `DELETE`
- **Path:** `/forms/:formId/responses`
- **Base URL:** `https://api.typeform.com`
- **Official documentation:** [Delete Responses](https://www.typeform.com/developers/responses/reference/delete-responses/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Typeform form identifier. |
| `included_response_ids` | query | `string` | no | Comma-separated list of response IDs to delete. |
| `included_response_ids` | body | `string` | no | — |
