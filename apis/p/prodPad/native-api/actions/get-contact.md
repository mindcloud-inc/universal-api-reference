# Get Contact with ProdPad

Retrieves a contact from ProdPad.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:id`
- **Base URL:** `https://api.prodpad.com/v1`
- **Official documentation:** [Get Contact](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/GetContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `feedbacks` | query | `boolean` | no | Include feedback provided by the contact in the response. |
