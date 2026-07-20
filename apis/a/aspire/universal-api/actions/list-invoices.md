# Aspire: List Invoices



```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-invoices?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressLine1": "string",
      "addressLine2": {},
      "amount": 1,
      "amountRemaining": 1,
      "billingContactID": 1,
      "billingContactName": "Ava Chen",
      "branchCode": "string",
      "branchID": 1,
      "branchName": "Ava Chen",
      "city": "string",
      "companyID": 1,
      "companyName": "Ava Chen",
      "completedDateTime": "string",
      "dueDate": "string",
      "emailStatus": "ava@example.com",
      "invoiceAccountingPeriod": {},
      "invoiceAddressID": 1,
      "invoiceBatchID": 1,
      "invoiceBatchNumber": 1,
      "invoiceDate": "string",
      "invoiceID": 1,
      "invoiceNote": {},
      "invoiceNumber": 1,
      "invoiceNumberPrefix": {},
      "invoiceOpportunities": [
        {
          "amount": 1,
          "customerContractNumber": {},
          "customerPONumber": {},
          "description": "string",
          "divisionName": "Ava Chen",
          "federalTaxAmount": 1,
          "federalTaxPercent": 1,
          "invoiceAdjustmentTypeID": {},
          "invoiceAdjustmentTypeName": {},
          "invoiceOpportunityID": 1,
          "invoiceType": "string",
          "opportunityID": 1,
          "opportunityName": "Ava Chen",
          "opportunityNumber": 1,
          "origAmount": 1,
          "origTotalAmount": 1,
          "retainagePercent": 1,
          "stateTaxAmount": 1,
          "stateTaxPercent": 1,
          "taxableAmount": 1,
          "totalAmount": 1
        }
      ],
      "lastModifiedByUserID": 1,
      "lastModifiedByUserName": "Ava Chen",
      "lastModifiedDateTime": "string",
      "origAmount": 1,
      "paymentTermsID": 1,
      "paymentTermsName": "Ava Chen",
      "primaryContactID": 1,
      "primaryContactName": "Ava Chen",
      "propertyID": 1,
      "propertyName": "Ava Chen",
      "reportLayoutID": 1,
      "reportLayoutName": "Ava Chen",
      "stateProvinceCode": "string",
      "taxJurisdictionID": 1,
      "taxJurisdictionName": "Ava Chen",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressLine1` | string |  |
| `addressLine2` | object |  |
| `amount` | number |  |
| `amountRemaining` | number |  |
| `billingContactID` | number |  |
| `billingContactName` | string |  |
| `branchCode` | string |  |
| `branchID` | number |  |
| `branchName` | string |  |
| `city` | string |  |
| `companyID` | number |  |
| `companyName` | string |  |
| `completedDateTime` | string |  |
| `dueDate` | string |  |
| `emailStatus` | string |  |
| `invoiceAccountingPeriod` | object |  |
| `invoiceAddressID` | number |  |
| `invoiceBatchID` | number |  |
| `invoiceBatchNumber` | number |  |
| `invoiceDate` | string |  |
| `invoiceID` | number |  |
| `invoiceNote` | object |  |
| `invoiceNumber` | number |  |
| `invoiceNumberPrefix` | object |  |
| `invoiceOpportunities[].amount` | number |  |
| `invoiceOpportunities[].customerContractNumber` | object |  |
| `invoiceOpportunities[].customerPONumber` | object |  |
| `invoiceOpportunities[].description` | string |  |
| `invoiceOpportunities[].divisionName` | string |  |
| `invoiceOpportunities[].federalTaxAmount` | number |  |
| `invoiceOpportunities[].federalTaxPercent` | number |  |
| `invoiceOpportunities[].invoiceAdjustmentTypeID` | object |  |
| `invoiceOpportunities[].invoiceAdjustmentTypeName` | object |  |
| `invoiceOpportunities[].invoiceOpportunityID` | number |  |
| `invoiceOpportunities[].invoiceType` | string |  |
| `invoiceOpportunities[].opportunityID` | number |  |
| `invoiceOpportunities[].opportunityName` | string |  |
| `invoiceOpportunities[].opportunityNumber` | number |  |
| `invoiceOpportunities[].origAmount` | number |  |
| `invoiceOpportunities[].origTotalAmount` | number |  |
| `invoiceOpportunities[].retainagePercent` | number |  |
| `invoiceOpportunities[].stateTaxAmount` | number |  |
| `invoiceOpportunities[].stateTaxPercent` | number |  |
| `invoiceOpportunities[].taxableAmount` | number |  |
| `invoiceOpportunities[].totalAmount` | number |  |
| `lastModifiedByUserID` | number |  |
| `lastModifiedByUserName` | string |  |
| `lastModifiedDateTime` | string |  |
| `origAmount` | number |  |
| `paymentTermsID` | number |  |
| `paymentTermsName` | string |  |
| `primaryContactID` | number |  |
| `primaryContactName` | string |  |
| `propertyID` | number |  |
| `propertyName` | string |  |
| `reportLayoutID` | number |  |
| `reportLayoutName` | string |  |
| `stateProvinceCode` | string |  |
| `taxJurisdictionID` | number |  |
| `taxJurisdictionName` | string |  |
| `zipCode` | string |  |

## Native endpoint

Through the native Aspire API, this operation is `GET invoices` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

