# Get Form Responses with BoloForms

Retrieves responses from a BoloForms form.

## Endpoint

- **Method:** `GET`
- **Path:** `/get-form-responses`
- **Base URL:** `https://sapi.boloforms.com/signature`
- **Official documentation:** [Get Form Responses](https://bolosign-developer-docs.readme.io/reference/get_get-form-responses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | query | `string` | yes | ID of the form to retrieve responses for |
| `responseId` | query | `string` | no | Specific response ID to retrieve |
| `page` | query | `number` | no | Page number for pagination |
| `limit` | query | `number` | no | Number of responses per page |
