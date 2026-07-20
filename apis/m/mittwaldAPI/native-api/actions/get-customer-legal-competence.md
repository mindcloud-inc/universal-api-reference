# Get Customer Legal Competence with mittwald

Retrieves a customer's legal competence status from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/customers/:customerId/legally-competent`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [Get Customer Legal Competence](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | The unique identifier of the customer. |
