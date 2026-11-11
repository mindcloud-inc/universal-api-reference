# Epicor Prophet 21: List Entity Customers



```
GET https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/list-entity-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Epicor Prophet 21 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/list-entity-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/list-entity-customers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "allowExceedJobQty": "string",
      "allowNonJobItem": "string",
      "alwaysUseJobPrice": "string",
      "billToContactId": "string",
      "class1id": "string",
      "class2id": "string",
      "class3id": "string",
      "class4id": "string",
      "class5id": "string",
      "codRequiredFlag": "string",
      "companyId": "string",
      "corporateCreditLimit": 1,
      "corporateCreditLimitAvailable": 1,
      "creditLimit": 1,
      "creditLimitAvailable": 1,
      "creditLimitCheckAtShipment": "string",
      "creditLimitPerOrder": 1,
      "creditLimitUsed": 1,
      "creditStatus": "string",
      "currencyId": 1,
      "customerId": 1,
      "customerName": "Ava Chen",
      "customerType": "string",
      "dateAcctOpened": "string",
      "defaultDisposition": "string",
      "delete": true,
      "excludeCanceldFromPackList": "string",
      "excludeCanceldFromPickTix": "string",
      "fcCycle": "string",
      "fcGraceDays": 1,
      "fcPercentage": 1,
      "federalExemptionNumber": "string",
      "freightChargeId": "string",
      "generateCustomerStatements": "string",
      "generateFinanceCharges": "string",
      "inclNonAllocOnListText": "string",
      "inclNonAllocOnTixText": "string",
      "interchgReceiverId": "string",
      "internationalSAN": "string",
      "invoiceBatchNumber": 1,
      "invoicePrintQty": 1,
      "jobNumberRequired": "string",
      "jobPricing": "string",
      "leadSourceId": "string",
      "legacyId": "string",
      "limitMaxShipmentsPerOrder": 1,
      "minimumFinanceCharge": 1,
      "minimumOrderDollarAmount": 1,
      "objectName": "Ava Chen",
      "orderAcknowledgments": "string",
      "orderPriorityId": "string",
      "otherExemptionNumber": "string",
      "overrideProfitLimit": "string",
      "overrideRevenueByItem": "string",
      "pickTicketType": "string",
      "poNoRequired": "string",
      "pricingMethod": "string",
      "printLotAttribOnInvoice": "string",
      "printLotAttribOnPacklist": "string",
      "printPackinglistInShipping": "string",
      "printPricesOnPackinglist": "string",
      "promiseDateBuffer": 1,
      "promptForNonJobItem": "string",
      "requirePaymentUponReleaseOfItems": true,
      "salesrepId": "string",
      "securityInfo": "string",
      "sendOutsideUseDocs": "string",
      "sendOutsideUseEmail": "ava@example.com",
      "sendOutsideUseFax": "string",
      "sendOutsideUsePrint": "string",
      "stateExciseTaxExemptionNo": "string",
      "statementBalance": "string",
      "statementBatchNumber": 1,
      "stateSalesTaxExemptionNo": "string",
      "taxable": "string",
      "termsId": "string",
      "tradingPartnerName": "Ava Chen",
      "upsHandlingCharge": 1,
      "useAllContracts": "string",
      "userDefinedFields": {},
      "useSystemUPSHandlingCharge": "string",
      "webEnabledFlag": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowExceedJobQty` | string |  |
| `allowNonJobItem` | string |  |
| `alwaysUseJobPrice` | string |  |
| `billToContactId` | string |  |
| `class1id` | string |  |
| `class2id` | string |  |
| `class3id` | string |  |
| `class4id` | string |  |
| `class5id` | string |  |
| `codRequiredFlag` | string |  |
| `companyId` | string |  |
| `corporateCreditLimit` | number |  |
| `corporateCreditLimitAvailable` | number |  |
| `creditLimit` | number |  |
| `creditLimitAvailable` | number |  |
| `creditLimitCheckAtShipment` | string |  |
| `creditLimitPerOrder` | number |  |
| `creditLimitUsed` | number |  |
| `creditStatus` | string |  |
| `currencyId` | number |  |
| `customerId` | number |  |
| `customerName` | string |  |
| `customerType` | string |  |
| `dateAcctOpened` | string |  |
| `defaultDisposition` | string |  |
| `delete` | boolean |  |
| `excludeCanceldFromPackList` | string |  |
| `excludeCanceldFromPickTix` | string |  |
| `fcCycle` | string |  |
| `fcGraceDays` | number |  |
| `fcPercentage` | number |  |
| `federalExemptionNumber` | string |  |
| `freightChargeId` | string |  |
| `generateCustomerStatements` | string |  |
| `generateFinanceCharges` | string |  |
| `inclNonAllocOnListText` | string |  |
| `inclNonAllocOnTixText` | string |  |
| `interchgReceiverId` | string |  |
| `internationalSAN` | string |  |
| `invoiceBatchNumber` | number |  |
| `invoicePrintQty` | number |  |
| `jobNumberRequired` | string |  |
| `jobPricing` | string |  |
| `leadSourceId` | string |  |
| `legacyId` | string |  |
| `limitMaxShipmentsPerOrder` | number |  |
| `minimumFinanceCharge` | number |  |
| `minimumOrderDollarAmount` | number |  |
| `objectName` | string |  |
| `orderAcknowledgments` | string |  |
| `orderPriorityId` | string |  |
| `otherExemptionNumber` | string |  |
| `overrideProfitLimit` | string |  |
| `overrideRevenueByItem` | string |  |
| `pickTicketType` | string |  |
| `poNoRequired` | string |  |
| `pricingMethod` | string |  |
| `printLotAttribOnInvoice` | string |  |
| `printLotAttribOnPacklist` | string |  |
| `printPackinglistInShipping` | string |  |
| `printPricesOnPackinglist` | string |  |
| `promiseDateBuffer` | number |  |
| `promptForNonJobItem` | string |  |
| `requirePaymentUponReleaseOfItems` | boolean |  |
| `salesrepId` | string |  |
| `securityInfo` | string |  |
| `sendOutsideUseDocs` | string |  |
| `sendOutsideUseEmail` | string |  |
| `sendOutsideUseFax` | string |  |
| `sendOutsideUsePrint` | string |  |
| `stateExciseTaxExemptionNo` | string |  |
| `statementBalance` | string |  |
| `statementBatchNumber` | number |  |
| `stateSalesTaxExemptionNo` | string |  |
| `taxable` | string |  |
| `termsId` | string |  |
| `tradingPartnerName` | string |  |
| `upsHandlingCharge` | number |  |
| `useAllContracts` | string |  |
| `userDefinedFields` | object |  |
| `useSystemUPSHandlingCharge` | string |  |
| `webEnabledFlag` | string |  |

## Native endpoint

Through the native Epicor Prophet 21 API, this operation is `GET /api/entity/customers/` (base URL `{{credentials.apiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-entity-customers.md) for the provider-specific parameters and requirements.

