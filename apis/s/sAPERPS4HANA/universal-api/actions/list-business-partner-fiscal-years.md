# SAP ERP (S/4HANA): List Business Partner Fiscal Years

Retrieves fiscal years for a business partner from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partner-fiscal-years
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partner-fiscal-years?connectionId=$CONNECTION_ID&businessPartner=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessPartner": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partner-fiscal-years?${params}`, {
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
      "BPAnnualNetIncAmtInBalShtCrcy": 1,
      "BPAnnualPnLAmtInBalShtCrcy": 1,
      "BPAnnualSalesAmtInBalShtCrcy": 1,
      "BPAnnualStockholderMeetingDate": "2026-05-07T12:00:00.000Z",
      "BPBalanceSheetCurrency": "string",
      "BPBalSheetTotalAmtInBalShtCrcy": 1,
      "BPCapitalStockAmtInBalShtCrcy": 1,
      "BPCptlReserveAmtInBalShtCrcy": 1,
      "BPDebtClearancePeriodInYears": 1,
      "BPDebtRatioInYears": 1,
      "BPDividendDistrAmtInBalShtCrcy": 1,
      "BPEquityCapitalAmtInBalShtCrcy": 1,
      "BPEquityRatioInPercent": 1,
      "BPFinancingCoeffInPercent": 1,
      "BPFiscalYearClosingDate": "2026-05-07T12:00:00.000Z",
      "BPFiscalYearEndDate": "2026-05-07T12:00:00.000Z",
      "BPFiscalYearIsClosed": true,
      "BPFiscalYearStartDate": "2026-05-07T12:00:00.000Z",
      "BPFsclYrCnsldtdFinStatementDte": "2026-05-07T12:00:00.000Z",
      "BPGrossPremiumAmtInBalShtCrcy": 1,
      "BPIssdStockCptlAmtInBalShtCrcy": 1,
      "BPLglRevnRsrvAmtInBalShtCrcy": 1,
      "BPNetPremiumAmtInBalShtCrcy": 1,
      "BPNumberOfEmployees": "string",
      "BPOthRevnRsrvAmtInBalShtCrcy": 1,
      "BPPartcipnCertAmtInBalShtCrcy": 1,
      "BPPnLCarryfwdAmtInBalShtCrcy": 1,
      "BPRetOnTotalCptlEmpldInPercent": 1,
      "BPStatryReserveAmtInBalShtCrcy": 1,
      "BPSuborddLbltyAmtInBalShtCrcy": 1,
      "BusinessPartner": "string",
      "BusinessPartnerFiscalYear": "string",
      "RevnRsrvOwnStkAmtInBalShtCrcy": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BPAnnualNetIncAmtInBalShtCrcy` | number |  |
| `BPAnnualPnLAmtInBalShtCrcy` | number |  |
| `BPAnnualSalesAmtInBalShtCrcy` | number |  |
| `BPAnnualStockholderMeetingDate` | date |  |
| `BPBalanceSheetCurrency` | string |  |
| `BPBalSheetTotalAmtInBalShtCrcy` | number |  |
| `BPCapitalStockAmtInBalShtCrcy` | number |  |
| `BPCptlReserveAmtInBalShtCrcy` | number |  |
| `BPDebtClearancePeriodInYears` | number |  |
| `BPDebtRatioInYears` | number |  |
| `BPDividendDistrAmtInBalShtCrcy` | number |  |
| `BPEquityCapitalAmtInBalShtCrcy` | number |  |
| `BPEquityRatioInPercent` | number |  |
| `BPFinancingCoeffInPercent` | number |  |
| `BPFiscalYearClosingDate` | date |  |
| `BPFiscalYearEndDate` | date |  |
| `BPFiscalYearIsClosed` | boolean |  |
| `BPFiscalYearStartDate` | date |  |
| `BPFsclYrCnsldtdFinStatementDte` | date |  |
| `BPGrossPremiumAmtInBalShtCrcy` | number |  |
| `BPIssdStockCptlAmtInBalShtCrcy` | number |  |
| `BPLglRevnRsrvAmtInBalShtCrcy` | number |  |
| `BPNetPremiumAmtInBalShtCrcy` | number |  |
| `BPNumberOfEmployees` | string |  |
| `BPOthRevnRsrvAmtInBalShtCrcy` | number |  |
| `BPPartcipnCertAmtInBalShtCrcy` | number |  |
| `BPPnLCarryfwdAmtInBalShtCrcy` | number |  |
| `BPRetOnTotalCptlEmpldInPercent` | number |  |
| `BPStatryReserveAmtInBalShtCrcy` | number |  |
| `BPSuborddLbltyAmtInBalShtCrcy` | number |  |
| `BusinessPartner` | string |  |
| `BusinessPartnerFiscalYear` | string |  |
| `RevnRsrvOwnStkAmtInBalShtCrcy` | number |  |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_BusinessPartner('{{businessPartner}}')/to_BPFiscalYearInformation` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-business-partner-fiscal-years.md) for the provider-specific parameters and requirements.

