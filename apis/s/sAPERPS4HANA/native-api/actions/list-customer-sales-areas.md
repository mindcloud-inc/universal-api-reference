# List Customer Sales Areas with SAP ERP (S/4HANA)

Retrieves customer sales areas from SAP ERP (S/4HANA).

## Endpoint

- **Method:** `GET`
- **Path:** `/A_CustomerSalesArea`
- **Base URL:** `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`
- **Official documentation:** [List Customer Sales Areas](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_CustomerSalesArea)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | Maximum number of customer sales areas to return. |
| `$skip` | query | `number` | no | Number of customer sales areas to skip before returning results. |
