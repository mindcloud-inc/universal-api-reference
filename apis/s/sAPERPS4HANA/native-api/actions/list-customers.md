# List Customers with SAP ERP (S/4HANA)

Retrieves customers from SAP ERP (S/4HANA).

## Endpoint

- **Method:** `GET`
- **Path:** `/A_Customer`
- **Base URL:** `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`
- **Official documentation:** [List Customers](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_Customer)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | Maximum number of customers to return. |
| `$skip` | query | `number` | no | Number of customers to skip before returning results. |
