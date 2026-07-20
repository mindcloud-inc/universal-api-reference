# List Customers with SOS Inventory

Retrieves customers from SOS Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/customer`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [List Customers](https://developer.sosinventory.com/apidoc/Customer)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `string` | no | Use yes to return archived records only or no to return active records only. |
| `email` | query | `string` | no | Filter by the customer's email. |
| `name` | query | `string` | no | Filter by matches on the name or fullname fields. |
| `query` | query | `string` | no | Filter by matches on name, fullname, or notes. |
