# List Customer Sales Area Taxes with SAP ERP (S/4HANA)

Retrieves customer sales area taxes from SAP ERP (S/4HANA).

## Endpoint

- **Method:** `GET`
- **Path:** `/A_CustomerSalesAreaTax`
- **Base URL:** `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`
- **Official documentation:** [List Customer Sales Area Taxes](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_CustomerSalesAreaTax)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | Maximum number of customer sales area tax records to return. |
| `$skip` | query | `number` | no | Number of customer sales area tax records to skip before returning results. |
