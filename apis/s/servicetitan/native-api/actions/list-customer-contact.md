# List Customer Contact with ServiceTitan

Retrieves contacts from ServiceTitan for a customer.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v2/tenant/{tenant}/customers/:contactId/contacts`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List Customer Contact](https://developer.servicetitan.io/api-details/#api=tenant-crm-v2&operation=Customers_GetContactList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contactId` | path | `string` | no |
| `includeTotal` | query | `boolean` | no |
