# Get Form Responses with Rowform

Retrieves form responses from Rowform.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/zapier/responses`
- **Base URL:** `https://app.rowform.io`
- **Official documentation:** [Get Form Responses](https://help.rowform.io/api-reference#get-form-responses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | query | `string` | yes | The Rowform form id to fetch responses for. |
| `limit` | query | `number` | no | Maximum number of responses to return. Rowform defaults to 25 and allows up to 100. |
