# Get Supplier for Business Partner with SAP ERP (S/4HANA)

Retrieves the supplier for a business partner from SAP ERP (S/4HANA).

## Endpoint

- **Method:** `GET`
- **Path:** `/A_BusinessPartner('{{businessPartner}}')/to_Supplier`
- **Base URL:** `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`
- **Official documentation:** [Get Supplier for Business Partner](https://api.sap.com/api/API_BUSINESS_PARTNER)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessPartner` | path | `string` | yes | Business partner identifier such as 11. |
