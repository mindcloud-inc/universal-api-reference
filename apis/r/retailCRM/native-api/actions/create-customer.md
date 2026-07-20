# Create Customer with retailCRM

Creates a new customer in retailCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/create`
- **Base URL:** `{accountUrl}/api/v5`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `site` | body | `list` | yes |
| `customer.externalId` | body | `string` | yes |
| `customer.firstName` | body | `string` | yes |
| `customer.lastName` | body | `string` | no |
| `customer.email` | body | `string` | no |
| `customer.phones[0].number` | body | `string` | yes |
| `customer.managerId` | body | `list` | no |
