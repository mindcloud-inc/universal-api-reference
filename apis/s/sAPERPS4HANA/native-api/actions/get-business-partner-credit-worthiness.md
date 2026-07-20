# Get Business Partner Credit Worthiness with SAP ERP (S/4HANA)

Retrieves credit worthiness for a business partner from SAP ERP (S/4HANA).

## Endpoint

- **Method:** `GET`
- **Path:** `/A_BusinessPartner('{{businessPartner}}')/to_BPCreditWorthiness`
- **Base URL:** `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`
- **Official documentation:** [Get Business Partner Credit Worthiness](https://api.sap.com/api/API_BUSINESS_PARTNER)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessPartner` | path | `string` | yes | Business partner identifier such as 11. |
