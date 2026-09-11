# List Customer Contact with ServiceTitan

Retrieves contacts from ServiceTitan for a customer.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v2/tenant/{tenant}/customers/:customerId/contacts`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List Customer Contact](https://developer.servicetitan.io/api-details/#api=tenant-crm-v2&operation=Customers_GetContactList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `string` | yes |
| `includeTotal` | query | `boolean` | no |
