# SAP ERP (S/4HANA): Get Supplier for Business Partner

Retrieves the supplier for a business partner from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/get-supplier-for-business-partner
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/get-supplier-for-business-partner?connectionId=$CONNECTION_ID&businessPartner=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessPartner": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/get-supplier-for-business-partner?${params}`, {
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
      "AlternativePayeeAccountNumber": "string",
      "AuthorizationGroup": "string",
      "BirthDate": "2026-05-07T12:00:00.000Z",
      "BR_TaxIsSplit": true,
      "BusinessPartnerPanNumber": "string",
      "ConcatenatedInternationalLocNo": "string",
      "CreatedByUser": "string",
      "CreationDate": "2026-05-07T12:00:00.000Z",
      "Customer": "string",
      "DataExchangeInstructionKey": "string",
      "DeletionIndicator": true,
      "FiscalAddress": "string",
      "Industry": "string",
      "InternationalLocationNumber1": "string",
      "InternationalLocationNumber2": "string",
      "InternationalLocationNumber3": "string",
      "IsNaturalPerson": "string",
      "JP_SuplrAmtInCapitalAmount": 1,
      "JP_SupplierCapitalAmountCrcy": "string",
      "PaymentIsBlockedForSupplier": true,
      "PaymentReason": "string",
      "PostingIsBlocked": true,
      "PurchasingIsBlocked": true,
      "ResponsibleType": "string",
      "SuplrProofOfDelivRlvtCode": "string",
      "SuplrQltyInProcmtCertfnValidTo": "2026-05-07T12:00:00.000Z",
      "SuplrQualityManagementSystem": "string",
      "Supplier": "string",
      "SupplierAccountGroup": "string",
      "SupplierCorporateGroup": "string",
      "SupplierFullName": "Ava Chen",
      "SupplierName": "Ava Chen",
      "SupplierProcurementBlock": "string",
      "TaxNumber1": "string",
      "TaxNumber2": "string",
      "TaxNumber3": "string",
      "TaxNumber4": "string",
      "TaxNumber5": "string",
      "TaxNumberResponsible": "string",
      "TaxNumberType": "string",
      "VATRegistration": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AlternativePayeeAccountNumber` | string |  |
| `AuthorizationGroup` | string |  |
| `BirthDate` | date |  |
| `BR_TaxIsSplit` | boolean |  |
| `BusinessPartnerPanNumber` | string |  |
| `ConcatenatedInternationalLocNo` | string |  |
| `CreatedByUser` | string |  |
| `CreationDate` | date |  |
| `Customer` | string |  |
| `DataExchangeInstructionKey` | string |  |
| `DeletionIndicator` | boolean |  |
| `FiscalAddress` | string |  |
| `Industry` | string |  |
| `InternationalLocationNumber1` | string |  |
| `InternationalLocationNumber2` | string |  |
| `InternationalLocationNumber3` | string |  |
| `IsNaturalPerson` | string |  |
| `JP_SuplrAmtInCapitalAmount` | number |  |
| `JP_SupplierCapitalAmountCrcy` | string |  |
| `PaymentIsBlockedForSupplier` | boolean |  |
| `PaymentReason` | string |  |
| `PostingIsBlocked` | boolean |  |
| `PurchasingIsBlocked` | boolean |  |
| `ResponsibleType` | string |  |
| `SuplrProofOfDelivRlvtCode` | string |  |
| `SuplrQltyInProcmtCertfnValidTo` | date |  |
| `SuplrQualityManagementSystem` | string |  |
| `Supplier` | string |  |
| `SupplierAccountGroup` | string |  |
| `SupplierCorporateGroup` | string |  |
| `SupplierFullName` | string |  |
| `SupplierName` | string |  |
| `SupplierProcurementBlock` | string |  |
| `TaxNumber1` | string |  |
| `TaxNumber2` | string |  |
| `TaxNumber3` | string |  |
| `TaxNumber4` | string |  |
| `TaxNumber5` | string |  |
| `TaxNumberResponsible` | string |  |
| `TaxNumberType` | string |  |
| `VATRegistration` | string |  |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_BusinessPartner('{{businessPartner}}')/to_Supplier` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-supplier-for-business-partner.md) for the provider-specific parameters and requirements.

