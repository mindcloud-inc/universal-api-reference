# Microsoft Dynamics 365 BC: List Customer Payment ODataV4 API V2



```
GET https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/list-customer-payment-o-data-v4-apiv2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 BC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/list-customer-payment-o-data-v4-apiv2?connectionId=$CONNECTION_ID&limit=25&offset=0&company='Active260127'" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "company": "'Active260127'"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/list-customer-payment-o-data-v4-apiv2?${params}`, {
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
| `company` | list | yes | One of: `'Active260127'`, `'Esser%20Plumbing%20%26%20Heating'`. |
| `$filter` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "no": "string",
      "name": "Ava Chen",
      "cFDICustomerName": "Ava Chen",
      "name2": "Ava Chen",
      "searchName": "Ava Chen",
      "iCPartnerCode": "string",
      "mAWMobilePhoneNo": "string",
      "balanceLCY": 1,
      "balanceAsVendor": 1,
      "balanceDueLCY": 1,
      "creditLimitLCY": 1,
      "blocked": "string",
      "privacyBlocked": true,
      "salespersonCode": "string",
      "responsibilityCenter": "string",
      "serviceZoneCode": "string",
      "documentSendingProfile": "string",
      "totalSales2": 1,
      "custSalesLCYCustProfitAdjmtCostLCY": 1,
      "adjCustProfit": 1,
      "adjProfitPct": 1,
      "mAWProductionOrderDefault": true,
      "mAWCalculateNAKTDue": true,
      "mAWAllowPVSDue": true,
      "mAWChamberOfCommerceNo": "string",
      "mAWAgentCode": "string",
      "mAWNoOfReceivedQuotes": 1,
      "mAWGlobalDimension1Code": "string",
      "mAWGlobalDimension2Code": "string",
      "mAWShortcutProperty1Value": "string",
      "mAWShortcutProperty2Value": "string",
      "mAWShortcutProperty3Value": "string",
      "mAWShortcutProperty4Value": "string",
      "mAWShortcutProperty5Value": "string",
      "mAWShortcutProperty6Value": "string",
      "mAWShortcutProperty7Value": "string",
      "mAWShortcutProperty8Value": "string",
      "mAWShortcutProperty9Value": "string",
      "mAWShortcutProperty10Value": "string",
      "cFDIPurpose": "string",
      "cFDIRelation": "string",
      "cFDIExportCode": "string",
      "sATTaxRegimeClassification": "string",
      "cFDIGeneralPublic": true,
      "cFDIPeriod": "string",
      "lastDateModified": "string",
      "disableSearchByName": true,
      "priority": 1,
      "statisticsGroup": 1,
      "address": "string",
      "address2": "string",
      "countryRegionCode": "string",
      "city": "string",
      "county": "string",
      "postCode": "string",
      "showMap": true,
      "phoneNo": "string",
      "mobilePhoneNo": "string",
      "eMail": "ava@example.com",
      "faxNo": "string",
      "homePage": "string",
      "languageCode": "string",
      "formatRegion": "string",
      "primaryContactNo": "string",
      "contactName": "Ava Chen",
      "mAWGrowersAssociation": "string",
      "mAWItemNoGMOSubsidyAmount": "string",
      "mAWGrowersAssociationCode": "string",
      "mAWGrowersAssociationName": "Ava Chen",
      "billToCustomerNo": "string",
      "vATRegistrationNo": "string",
      "eORINumber": "string",
      "gln": "string",
      "useGLNInElectronicDocument": true,
      "copySellToAddrToQteFrom": true,
      "taxLiable": true,
      "taxAreaCode": "string",
      "taxIdentificationType": "string",
      "taxExemptionNo": "string",
      "rFCNo": "string",
      "cURPNo": "string",
      "stateInscription": "string",
      "registrationNumber": "string",
      "genBusPostingGroup": "string",
      "vATBusPostingGroup": "string",
      "customerPostingGroup": "string",
      "allowMultiplePostingGroups": true,
      "currencyCode": "string",
      "priceCalculationMethod": "string",
      "customerPriceGroup": "string",
      "customerDiscGroup": "string",
      "allowLineDisc": true,
      "invoiceDiscCode": "string",
      "pricesIncludingVAT": true,
      "eDocumentServiceParticipationIds": "string",
      "prepaymentPercent": 1,
      "applicationMethod": "string",
      "partnerType": "string",
      "intrastatPartnerType": "string",
      "paymentTermsCode": "string",
      "paymentMethodCode": "string",
      "reminderTermsCode": "string",
      "finChargeTermsCode": "string",
      "cashFlowPaymentTermsCode": "string",
      "printStatements": true,
      "lastStatementNo": 1,
      "blockPaymentTolerance": true,
      "preferredBankAccountCode": "string",
      "bankCommunication": true,
      "checkDateFormat": "string",
      "checkDateSeparator": "string",
      "excludeFromPmtPractices": true,
      "shipToCode": "string",
      "locationCode": "string",
      "combineShipments": true,
      "combineServiceShipments": true,
      "reserve": "string",
      "mAWEntryPoint": "string",
      "mAWTerritoryCode": "string",
      "mAWCalculateTransportCosts": true,
      "shippingAdvice": "string",
      "shipmentMethodCode": "string",
      "shippingAgentCode": "string",
      "shippingAgentServiceCode": "string",
      "shippingTime": "string",
      "baseCalendarCode": "string",
      "customizedCalendar": "string",
      "mAWLDeliveryInstruction": "string",
      "customerSince": "string",
      "daysSinceLastSale": 1,
      "distinctItemsSold": 1,
      "balanceLCY2": 1,
      "expectedCustMoneyOwed": 1,
      "totalMoneyOwed": 1,
      "creditLimit": 1,
      "calcCreditLimitLCYExpendedPct": 1,
      "balanceDue": 1,
      "paymentsLCY": 1,
      "customerMgtAvgDaysToPayNo": 1,
      "daysPaidPastDueDate": 1,
      "paidLateCount": 1,
      "paidOnTimeCount": 1,
      "percentPaidLate": 1,
      "overdueCount": 1,
      "lastPaymentDate": "string",
      "lastPaymentAmount": 1,
      "lastPaymentOnTime": true,
      "amountOnPostedInvoices": 1,
      "amountOnCrMemo": 1,
      "amountOnOutstandingInvoices": 1,
      "amountOnOutstandingCrMemos": 1,
      "totals": {},
      "custInvDiscAmountLCY": 1,
      "interactionCount": 1,
      "lastInteractionDate": "string",
      "lastInteractionType": "string",
      "mostFrequentInteractionType": "string",
      "globalDimension1Filter": "string",
      "globalDimension2Filter": "string",
      "currencyFilter": "string",
      "dateFilter": "string",
      "mAWContactFilter": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `no` | string |  |
| `name` | string |  |
| `cFDICustomerName` | string |  |
| `name2` | string |  |
| `searchName` | string |  |
| `iCPartnerCode` | string |  |
| `mAWMobilePhoneNo` | string |  |
| `balanceLCY` | number |  |
| `balanceAsVendor` | number |  |
| `balanceDueLCY` | number |  |
| `creditLimitLCY` | number |  |
| `blocked` | string |  |
| `privacyBlocked` | boolean |  |
| `salespersonCode` | string |  |
| `responsibilityCenter` | string |  |
| `serviceZoneCode` | string |  |
| `documentSendingProfile` | string |  |
| `totalSales2` | number |  |
| `custSalesLCYCustProfitAdjmtCostLCY` | number |  |
| `adjCustProfit` | number |  |
| `adjProfitPct` | number |  |
| `mAWProductionOrderDefault` | boolean |  |
| `mAWCalculateNAKTDue` | boolean |  |
| `mAWAllowPVSDue` | boolean |  |
| `mAWChamberOfCommerceNo` | string |  |
| `mAWAgentCode` | string |  |
| `mAWNoOfReceivedQuotes` | number |  |
| `mAWGlobalDimension1Code` | string |  |
| `mAWGlobalDimension2Code` | string |  |
| `mAWShortcutProperty1Value` | string |  |
| `mAWShortcutProperty2Value` | string |  |
| `mAWShortcutProperty3Value` | string |  |
| `mAWShortcutProperty4Value` | string |  |
| `mAWShortcutProperty5Value` | string |  |
| `mAWShortcutProperty6Value` | string |  |
| `mAWShortcutProperty7Value` | string |  |
| `mAWShortcutProperty8Value` | string |  |
| `mAWShortcutProperty9Value` | string |  |
| `mAWShortcutProperty10Value` | string |  |
| `cFDIPurpose` | string |  |
| `cFDIRelation` | string |  |
| `cFDIExportCode` | string |  |
| `sATTaxRegimeClassification` | string |  |
| `cFDIGeneralPublic` | boolean |  |
| `cFDIPeriod` | string |  |
| `lastDateModified` | string |  |
| `disableSearchByName` | boolean |  |
| `priority` | number |  |
| `statisticsGroup` | number |  |
| `address` | string |  |
| `address2` | string |  |
| `countryRegionCode` | string |  |
| `city` | string |  |
| `county` | string |  |
| `postCode` | string |  |
| `showMap` | boolean |  |
| `phoneNo` | string |  |
| `mobilePhoneNo` | string |  |
| `eMail` | string |  |
| `faxNo` | string |  |
| `homePage` | string |  |
| `languageCode` | string |  |
| `formatRegion` | string |  |
| `primaryContactNo` | string |  |
| `contactName` | string |  |
| `mAWGrowersAssociation` | string |  |
| `mAWItemNoGMOSubsidyAmount` | string |  |
| `mAWGrowersAssociationCode` | string |  |
| `mAWGrowersAssociationName` | string |  |
| `billToCustomerNo` | string |  |
| `vATRegistrationNo` | string |  |
| `eORINumber` | string |  |
| `gln` | string |  |
| `useGLNInElectronicDocument` | boolean |  |
| `copySellToAddrToQteFrom` | boolean |  |
| `taxLiable` | boolean |  |
| `taxAreaCode` | string |  |
| `taxIdentificationType` | string |  |
| `taxExemptionNo` | string |  |
| `rFCNo` | string |  |
| `cURPNo` | string |  |
| `stateInscription` | string |  |
| `registrationNumber` | string |  |
| `genBusPostingGroup` | string |  |
| `vATBusPostingGroup` | string |  |
| `customerPostingGroup` | string |  |
| `allowMultiplePostingGroups` | boolean |  |
| `currencyCode` | string |  |
| `priceCalculationMethod` | string |  |
| `customerPriceGroup` | string |  |
| `customerDiscGroup` | string |  |
| `allowLineDisc` | boolean |  |
| `invoiceDiscCode` | string |  |
| `pricesIncludingVAT` | boolean |  |
| `eDocumentServiceParticipationIds` | string |  |
| `prepaymentPercent` | number |  |
| `applicationMethod` | string |  |
| `partnerType` | string |  |
| `intrastatPartnerType` | string |  |
| `paymentTermsCode` | string |  |
| `paymentMethodCode` | string |  |
| `reminderTermsCode` | string |  |
| `finChargeTermsCode` | string |  |
| `cashFlowPaymentTermsCode` | string |  |
| `printStatements` | boolean |  |
| `lastStatementNo` | number |  |
| `blockPaymentTolerance` | boolean |  |
| `preferredBankAccountCode` | string |  |
| `bankCommunication` | boolean |  |
| `checkDateFormat` | string |  |
| `checkDateSeparator` | string |  |
| `excludeFromPmtPractices` | boolean |  |
| `shipToCode` | string |  |
| `locationCode` | string |  |
| `combineShipments` | boolean |  |
| `combineServiceShipments` | boolean |  |
| `reserve` | string |  |
| `mAWEntryPoint` | string |  |
| `mAWTerritoryCode` | string |  |
| `mAWCalculateTransportCosts` | boolean |  |
| `shippingAdvice` | string |  |
| `shipmentMethodCode` | string |  |
| `shippingAgentCode` | string |  |
| `shippingAgentServiceCode` | string |  |
| `shippingTime` | string |  |
| `baseCalendarCode` | string |  |
| `customizedCalendar` | string |  |
| `mAWLDeliveryInstruction` | string |  |
| `customerSince` | string |  |
| `daysSinceLastSale` | number |  |
| `distinctItemsSold` | number |  |
| `balanceLCY2` | number |  |
| `expectedCustMoneyOwed` | number |  |
| `totalMoneyOwed` | number |  |
| `creditLimit` | number |  |
| `calcCreditLimitLCYExpendedPct` | number |  |
| `balanceDue` | number |  |
| `paymentsLCY` | number |  |
| `customerMgtAvgDaysToPayNo` | number |  |
| `daysPaidPastDueDate` | number |  |
| `paidLateCount` | number |  |
| `paidOnTimeCount` | number |  |
| `percentPaidLate` | number |  |
| `overdueCount` | number |  |
| `lastPaymentDate` | string |  |
| `lastPaymentAmount` | number |  |
| `lastPaymentOnTime` | boolean |  |
| `amountOnPostedInvoices` | number |  |
| `amountOnCrMemo` | number |  |
| `amountOnOutstandingInvoices` | number |  |
| `amountOnOutstandingCrMemos` | number |  |
| `totals` | object |  |
| `custInvDiscAmountLCY` | number |  |
| `interactionCount` | number |  |
| `lastInteractionDate` | string |  |
| `lastInteractionType` | string |  |
| `mostFrequentInteractionType` | string |  |
| `globalDimension1Filter` | string |  |
| `globalDimension2Filter` | string |  |
| `currencyFilter` | string |  |
| `dateFilter` | string |  |
| `mAWContactFilter` | string |  |

## Native endpoint

Through the native Microsoft Dynamics 365 BC API, this operation is `GET https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/MindcloudCustomerPayments` (base URL `https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customer-payment-o-data-v4-apiv2.md) for the provider-specific parameters and requirements.

