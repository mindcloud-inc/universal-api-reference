# List Supplier Withholding Taxes with SAP ERP (S/4HANA)

Retrieves supplier withholding taxes from SAP ERP (S/4HANA).

## Endpoint

- **Method:** `GET`
- **Path:** `/A_SupplierWithHoldingTax`
- **Base URL:** `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`
- **Official documentation:** [List Supplier Withholding Taxes](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_SupplierWithHoldingTax)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | Maximum number of supplier withholding tax records to return. |
| `$skip` | query | `number` | no | Number of supplier withholding tax records to skip before returning results. |
