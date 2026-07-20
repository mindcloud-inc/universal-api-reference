# List Business Partners with SAP ERP (S/4HANA)

Retrieves business partners from SAP ERP (S/4HANA).

## Endpoint

- **Method:** `GET`
- **Path:** `/A_BusinessPartner`
- **Base URL:** `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`
- **Official documentation:** [List Business Partners](https://api.sap.com/api/API_BUSINESS_PARTNER/resource/A_BusinessPartner)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | Maximum number of business partners to return for the list request. |
