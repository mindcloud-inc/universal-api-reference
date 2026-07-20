# SAP ERP (S/4HANA): Get Customer for Business Partner

Retrieves the customer for a business partner from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/get-customer-for-business-partner
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/get-customer-for-business-partner?connectionId=$CONNECTION_ID&businessPartner=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessPartner": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/get-customer-for-business-partner?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessPartner` | string | yes | Business partner identifier such as 11. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AuthorizationGroup": "string",
      "BillingIsBlockedForCustomer": "string",
      "BPCustomerFullName": "Ava Chen",
      "BPCustomerName": "Ava Chen",
      "BR_ICMSTaxPayerType": "string",
      "CityCode": "string",
      "County": "string",
      "CreatedByUser": "string",
      "CreationDate": "2026-05-07T12:00:00.000Z",
      "Customer": "string",
      "CustomerAccountGroup": "string",
      "CustomerClassification": "string",
      "CustomerCorporateGroup": "string",
      "CustomerFullName": "Ava Chen",
      "CustomerName": "Ava Chen",
      "DeletionIndicator": true,
      "DeliveryIsBlocked": "string",
      "ExpressTrainStationName": "Ava Chen",
      "FiscalAddress": "string",
      "FreeDefinedAttribute01": "string",
      "FreeDefinedAttribute02": "string",
      "FreeDefinedAttribute03": "string",
      "FreeDefinedAttribute04": "string",
      "FreeDefinedAttribute05": "string",
      "FreeDefinedAttribute06": "string",
      "FreeDefinedAttribute07": "string",
      "FreeDefinedAttribute08": "string",
      "FreeDefinedAttribute09": "string",
      "FreeDefinedAttribute10": "string",
      "Industry": "string",
      "IndustryCode1": "string",
      "IndustryCode2": "string",
      "IndustryCode3": "string",
      "IndustryCode4": "string",
      "IndustryCode5": "string",
      "InternationalLocationNumber1": "string",
      "InternationalLocationNumber2": "string",
      "InternationalLocationNumber3": "string",
      "NFPartnerIsNaturalPerson": "string",
      "NielsenRegion": "string",
      "OrderIsBlockedForCustomer": "string",
      "PaymentReason": "string",
      "PostingIsBlocked": true,
      "ResponsibleType": "string",
      "Supplier": "string",
      "TaxNumber1": "string",
      "TaxNumber2": "string",
      "TaxNumber3": "string",
      "TaxNumber4": "string",
      "TaxNumber5": "string",
      "TaxNumberType": "string",
      "TrainStationName": "Ava Chen",
      "VATRegistration": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AuthorizationGroup` | string |  |
| `BillingIsBlockedForCustomer` | string |  |
| `BPCustomerFullName` | string |  |
| `BPCustomerName` | string |  |
| `BR_ICMSTaxPayerType` | string |  |
| `CityCode` | string |  |
| `County` | string |  |
| `CreatedByUser` | string |  |
| `CreationDate` | date |  |
| `Customer` | string |  |
| `CustomerAccountGroup` | string |  |
| `CustomerClassification` | string |  |
| `CustomerCorporateGroup` | string |  |
| `CustomerFullName` | string |  |
| `CustomerName` | string |  |
| `DeletionIndicator` | boolean |  |
| `DeliveryIsBlocked` | string |  |
| `ExpressTrainStationName` | string |  |
| `FiscalAddress` | string |  |
| `FreeDefinedAttribute01` | string |  |
| `FreeDefinedAttribute02` | string |  |
| `FreeDefinedAttribute03` | string |  |
| `FreeDefinedAttribute04` | string |  |
| `FreeDefinedAttribute05` | string |  |
| `FreeDefinedAttribute06` | string |  |
| `FreeDefinedAttribute07` | string |  |
| `FreeDefinedAttribute08` | string |  |
| `FreeDefinedAttribute09` | string |  |
| `FreeDefinedAttribute10` | string |  |
| `Industry` | string |  |
| `IndustryCode1` | string |  |
| `IndustryCode2` | string |  |
| `IndustryCode3` | string |  |
| `IndustryCode4` | string |  |
| `IndustryCode5` | string |  |
| `InternationalLocationNumber1` | string |  |
| `InternationalLocationNumber2` | string |  |
| `InternationalLocationNumber3` | string |  |
| `NFPartnerIsNaturalPerson` | string |  |
| `NielsenRegion` | string |  |
| `OrderIsBlockedForCustomer` | string |  |
| `PaymentReason` | string |  |
| `PostingIsBlocked` | boolean |  |
| `ResponsibleType` | string |  |
| `Supplier` | string |  |
| `TaxNumber1` | string |  |
| `TaxNumber2` | string |  |
| `TaxNumber3` | string |  |
| `TaxNumber4` | string |  |
| `TaxNumber5` | string |  |
| `TaxNumberType` | string |  |
| `TrainStationName` | string |  |
| `VATRegistration` | string |  |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_BusinessPartner('{{businessPartner}}')/to_Customer` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-for-business-partner.md) for the provider-specific parameters and requirements.

