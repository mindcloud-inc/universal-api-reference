# List Vendors with SOS Inventory

Retrieves vendors from SOS Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/vendor`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [List Vendors](https://developer.sosinventory.com/apidoc/Vendor)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `string` | no | Use yes to return archived records only or no to return active records only. |
| `query` | query | `string` | no | Filter by matches on the vendor name or notes. |
