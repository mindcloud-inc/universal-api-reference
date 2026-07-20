# List Supplier Partner Functions with SAP ERP (S/4HANA)

Retrieves supplier partner functions from SAP ERP (S/4HANA).

## Endpoint

- **Method:** `GET`
- **Path:** `/A_SupplierPartnerFunc`
- **Base URL:** `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`
- **Official documentation:** [List Supplier Partner Functions](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_SupplierPartnerFunc)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | Maximum number of supplier partner functions to return. |
| `$skip` | query | `number` | no | Number of supplier partner functions to skip before returning results. |
