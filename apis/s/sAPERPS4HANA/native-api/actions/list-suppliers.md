# List Suppliers with SAP ERP (S/4HANA)

Retrieves suppliers from SAP ERP (S/4HANA).

## Endpoint

- **Method:** `GET`
- **Path:** `/A_Supplier`
- **Base URL:** `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`
- **Official documentation:** [List Suppliers](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_Supplier)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | Maximum number of suppliers to return. |
| `$skip` | query | `number` | no | Number of suppliers to skip before returning results. |
