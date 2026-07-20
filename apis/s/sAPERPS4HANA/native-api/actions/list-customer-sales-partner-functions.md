# List Customer Sales Partner Functions with SAP ERP (S/4HANA)

Retrieves customer sales partner functions from SAP ERP (S/4HANA).

## Endpoint

- **Method:** `GET`
- **Path:** `/A_CustSalesPartnerFunc`
- **Base URL:** `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`
- **Official documentation:** [List Customer Sales Partner Functions](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_CustSalesPartnerFunc)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | Maximum number of customer sales partner functions to return. |
| `$skip` | query | `number` | no | Number of customer sales partner functions to skip before returning results. |
