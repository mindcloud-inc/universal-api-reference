# SAP ERP (S/4HANA): List Business Partner Financial Reports

Retrieves financial reports for a business partner from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partner-financial-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partner-financial-reports?connectionId=$CONNECTION_ID&businessPartner=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessPartner": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partner-financial-reports?${params}`, {
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
      "BPCentralBankCountryRegion": "string",
      "BPCompanyRelationship": "string",
      "BPCrdtStandingReviewIsRequired": true,
      "BPCreditStandingReview": "string",
      "BPCreditStandingReviewDate": "2026-05-07T12:00:00.000Z",
      "BPGerAstRglnRestrictedAstQuota": "string",
      "BPGroupAssignmentCategory": "string",
      "BPHasCreditingRelief": true,
      "BPHasGroupAffiliation": true,
      "BPInvestInRstrcdAstIsAuthzd": true,
      "BPIsMonetaryFinInstitution": true,
      "BPIsMultimillionLoanRecipient": true,
      "BPIsNonResident": true,
      "BPLoanMonitoringIsRequired": true,
      "BPLoanReportingBorrowerNumber": "string",
      "BPLoanReportingCreditorNumber": "string",
      "BPLoanRptgBorrowerEntityNumber": "string",
      "BPNonResidencyStartDate": "2026-05-07T12:00:00.000Z",
      "BPOeNBIdentNumber": "string",
      "BPOeNBIdentNumberAssigned": "string",
      "BPOeNBInstituteNumber": "string",
      "BPOeNBTargetGroup": "string",
      "BPRiskGroupingDate": "2026-05-07T12:00:00.000Z",
      "BusinessPartner": "string",
      "BusinessPartnerBusinessPurpose": "string",
      "BusinessPartnerDebtorGroup": "string",
      "BusinessPartnerGroup": "string",
      "BusinessPartnerGroupName": "Ava Chen",
      "BusinessPartnerIsOeNBInstitute": true,
      "BusinessPartnerLegalEntity": "string",
      "BusinessPartnerLoanToManager": "string",
      "BusinessPartnerRiskGroup": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BPCentralBankCountryRegion` | string |  |
| `BPCompanyRelationship` | string |  |
| `BPCrdtStandingReviewIsRequired` | boolean |  |
| `BPCreditStandingReview` | string |  |
| `BPCreditStandingReviewDate` | date |  |
| `BPGerAstRglnRestrictedAstQuota` | string |  |
| `BPGroupAssignmentCategory` | string |  |
| `BPHasCreditingRelief` | boolean |  |
| `BPHasGroupAffiliation` | boolean |  |
| `BPInvestInRstrcdAstIsAuthzd` | boolean |  |
| `BPIsMonetaryFinInstitution` | boolean |  |
| `BPIsMultimillionLoanRecipient` | boolean |  |
| `BPIsNonResident` | boolean |  |
| `BPLoanMonitoringIsRequired` | boolean |  |
| `BPLoanReportingBorrowerNumber` | string |  |
| `BPLoanReportingCreditorNumber` | string |  |
| `BPLoanRptgBorrowerEntityNumber` | string |  |
| `BPNonResidencyStartDate` | date |  |
| `BPOeNBIdentNumber` | string |  |
| `BPOeNBIdentNumberAssigned` | string |  |
| `BPOeNBInstituteNumber` | string |  |
| `BPOeNBTargetGroup` | string |  |
| `BPRiskGroupingDate` | date |  |
| `BusinessPartner` | string |  |
| `BusinessPartnerBusinessPurpose` | string |  |
| `BusinessPartnerDebtorGroup` | string |  |
| `BusinessPartnerGroup` | string |  |
| `BusinessPartnerGroupName` | string |  |
| `BusinessPartnerIsOeNBInstitute` | boolean |  |
| `BusinessPartnerLegalEntity` | string |  |
| `BusinessPartnerLoanToManager` | string |  |
| `BusinessPartnerRiskGroup` | string |  |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_BusinessPartner('{{businessPartner}}')/to_BPFinServicesReporting` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-business-partner-financial-reports.md) for the provider-specific parameters and requirements.

