# List Customers with MILKEE

Retrieves customers from MILKEE.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/customers`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [List Customers](https://apidocs.milkee.ch/api/resources/customers.html#alle-customers-auflisten)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
