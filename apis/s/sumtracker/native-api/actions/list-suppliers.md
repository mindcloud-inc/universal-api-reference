# List Suppliers with Sumtracker

Retrieves suppliers from Sumtracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/version/2025-03/purchases/contacts/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [List Suppliers](https://developers.sumtracker.com/reference/supplierlist)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | query | `string` | no | Supplier code. |
| `company_name` | query | `string` | no | Supplier company name. |
