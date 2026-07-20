# Get Business Partner with SAP ERP (S/4HANA)

Retrieves a business partner from SAP ERP (S/4HANA).

## Endpoint

- **Method:** `GET`
- **Path:** `/A_BusinessPartner('{{businessPartner}}')`
- **Base URL:** `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`
- **Official documentation:** [Get Business Partner](https://api.sap.com/api/API_BUSINESS_PARTNER)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessPartner` | path | `string` | yes | Business partner identifier such as 11. |
