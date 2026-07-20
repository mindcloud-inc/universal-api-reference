# List Customers with Qualiobee

Retrieves customers from Qualiobee.

## Endpoint

- **Method:** `GET`
- **Path:** `/:organizationUuid/customer`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [List Customers](https://app.qualiobee.fr/api/doc/#/Customer/PublicCustomerController_getMany)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes | The Qualiobee organization UUID used in the request path |
| `relations` | query | `list<string>` | no | Related entities to include in each customer response Send multiple values as a array. |
| `uuid` | query | `string` | no | Filter customers by UUID |
| `externalId` | query | `string` | no | Filter customers by external ID |
| `name` | query | `string` | no | Filter customers by name |
| `firstName` | query | `string` | no | Filter customers by referent or individual first name |
| `lastName` | query | `string` | no | Filter customers by referent or individual last name |
| `email` | query | `string` | no | Filter customers by referent or individual email |
| `isIndividual` | query | `string` | no | Filter results to individual customers or companies |
| `withDeleted` | query | `boolean` | no | Include deleted customers in the results |
