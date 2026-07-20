# List Address-Dependent Tax Numbers with SAP ERP (S/4HANA)

Retrieves address-dependent tax numbers from SAP ERP (S/4HANA).

## Endpoint

- **Method:** `GET`
- **Path:** `/A_BusinessPartner('{{businessPartner}}')/to_BusPartAddrDepdntTaxNmbr`
- **Base URL:** `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`
- **Official documentation:** [List Address-Dependent Tax Numbers](https://api.sap.com/api/API_BUSINESS_PARTNER)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessPartner` | path | `string` | yes | Business partner identifier such as 11. |
