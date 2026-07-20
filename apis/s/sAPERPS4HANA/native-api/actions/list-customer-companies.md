# List Customer Companies with SAP ERP (S/4HANA)

Retrieves customer companies from SAP ERP (S/4HANA).

## Endpoint

- **Method:** `GET`
- **Path:** `/A_CustomerCompany`
- **Base URL:** `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`
- **Official documentation:** [List Customer Companies](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_CustomerCompany)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | Maximum number of customer company records to return. |
| `$skip` | query | `number` | no | Number of customer company records to skip before returning results. |
