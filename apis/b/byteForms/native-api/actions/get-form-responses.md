# Get Form Responses with ByteForms

Retrieves responses for a ByteForms form by form ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/form/responses/:formId`
- **Base URL:** `https://api.forms.bytesuite.io/`
- **Official documentation:** [Get Form Responses](https://forms.bytesuite.io/docs/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `after` | query | `string` | no |
| `before` | query | `string` | no |
| `formId` | path | `string` | no |
| `limit` | query | `string` | no |
| `order` | query | `string` | no |
| `query` | query | `string` | no |
