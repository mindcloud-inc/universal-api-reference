# List Supplier Purchasing Organizations with SAP ERP (S/4HANA)

Retrieves supplier purchasing organizations from SAP ERP (S/4HANA).

## Endpoint

- **Method:** `GET`
- **Path:** `/A_SupplierPurchasingOrg`
- **Base URL:** `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`
- **Official documentation:** [List Supplier Purchasing Organizations](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_SupplierPurchasingOrg)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | Maximum number of supplier purchasing organizations to return. |
| `$skip` | query | `number` | no | Number of supplier purchasing organizations to skip before returning results. |
