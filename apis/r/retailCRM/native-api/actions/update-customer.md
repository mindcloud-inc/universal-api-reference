# Update Customer with retailCRM

Updates an existing customer in retailCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/:externalId/edit`
- **Base URL:** `{accountUrl}/api/v5`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | path | `string` | yes | — |
| `by` | body | `list` | no | Accepted values: `externalId`, `id`. |
| `site` | body | `list` | yes | — |
| `customer.firstName` | body | `string` | no | — |
| `customer.lastName` | body | `string` | no | — |
| `customer.email` | body | `string` | no | — |
| `customer.phones[0].number` | body | `string` | no | — |
| `customer.managerId` | body | `list` | no | — |
