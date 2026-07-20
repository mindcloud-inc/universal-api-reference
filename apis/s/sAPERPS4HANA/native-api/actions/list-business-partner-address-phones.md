# List Business Partner Address Phones with SAP ERP (S/4HANA)

Retrieves business partner address phones from SAP ERP (S/4HANA).

## Endpoint

- **Method:** `GET`
- **Path:** `/A_BusinessPartnerAddress(BusinessPartner='{{businessPartner}}',AddressID='{{addressId}}')/to_PhoneNumber`
- **Base URL:** `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`
- **Official documentation:** [List Business Partner Address Phones](https://api.sap.com/api/API_BUSINESS_PARTNER)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addressId` | path | `string` | yes | Address identifier such as 27512. |
| `businessPartner` | path | `string` | yes | Business partner identifier such as 11. |
