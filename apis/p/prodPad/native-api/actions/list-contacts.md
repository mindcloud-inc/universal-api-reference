# List Contacts with ProdPad

Retrieves contacts from ProdPad.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.prodpad.com/v1`
- **Official documentation:** [List Contacts](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/GetContacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | query | `string` | no | — |
| `persona` | query | `string` | no | — |
| `job_role` | query | `string` | no | — |
| `tags` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `name` | query | `string` | no | — |
| `external_id` | query | `string` | no | — |
| `external_url` | query | `string` | no | — |
| `email` | query | `string` | no | — |
| `feedbacks` | query | `boolean` | no | — |
