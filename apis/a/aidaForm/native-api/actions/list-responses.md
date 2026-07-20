# List Responses with AidaForm

Retrieves form responses from AidaForm by form ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId/responses`
- **Base URL:** `https://api.aidaform.com/v1`
- **Official documentation:** [List Responses](https://app.swaggerhub.com/apis/aidaform/AidaForm/1.0.1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Use the top-level form UUID from List Forms.id. Do not use the short code in data.code. |
| `from` | query | `number` | no | Only include responses not older than this Unix timestamp. |
| `to` | query | `number` | no | Only include responses not newer than this Unix timestamp. |
| `limit` | query | `number` | no | Maximum number of responses to return. |
| `marker` | query | `string` | no | Pagination marker for the next page of responses. |
