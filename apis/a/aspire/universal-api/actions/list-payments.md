# Aspire: List Payments



```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-payments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-payments?${params}`, {
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
      "bankDepositID": {},
      "billingAddressID": 1,
      "branchID": 1,
      "branchName": "Ava Chen",
      "companyID": 1,
      "companyName": "Ava Chen",
      "contactID": 1,
      "contactName": "Ava Chen",
      "createdByUserID": 1,
      "createdByUserName": "Ava Chen",
      "createdDateTime": "string",
      "creditMemoNumber": 1,
      "divisionID": 1,
      "divisionName": "Ava Chen",
      "electronicPaymentID": {},
      "emailStatus": {},
      "isExpense": true,
      "lastModifiedByUserID": 1,
      "lastModifiedByUserName": "Ava Chen",
      "lastModifiedDateTime": "string",
      "opportunityID": {},
      "paymentAllocations": [
        {
          "amount": 1,
          "createdByUserID": 1,
          "createdByUserName": "Ava Chen",
          "createdDateTime": "string",
          "invoiceID": 1,
          "invoiceNumber": 1,
          "paymentAllocationID": 1
        }
      ],
      "paymentAmount": 1,
      "paymentCategoryID": {},
      "paymentCategoryName": {},
      "paymentDate": "string",
      "paymentID": 1,
      "paymentNote": {},
      "paymentReference": {},
      "paymentType": "string",
      "propertyID": 1,
      "saleAmount": 1,
      "taxableAmount": 1,
      "taxAmount": 1,
      "taxJurisdictionID": 1,
      "taxJurisdictionName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bankDepositID` | object |  |
| `billingAddressID` | number |  |
| `branchID` | number |  |
| `branchName` | string |  |
| `companyID` | number |  |
| `companyName` | string |  |
| `contactID` | number |  |
| `contactName` | string |  |
| `createdByUserID` | number |  |
| `createdByUserName` | string |  |
| `createdDateTime` | string |  |
| `creditMemoNumber` | number |  |
| `divisionID` | number |  |
| `divisionName` | string |  |
| `electronicPaymentID` | object |  |
| `emailStatus` | object |  |
| `isExpense` | boolean |  |
| `lastModifiedByUserID` | number |  |
| `lastModifiedByUserName` | string |  |
| `lastModifiedDateTime` | string |  |
| `opportunityID` | object |  |
| `paymentAllocations[].amount` | number |  |
| `paymentAllocations[].createdByUserID` | number |  |
| `paymentAllocations[].createdByUserName` | string |  |
| `paymentAllocations[].createdDateTime` | string |  |
| `paymentAllocations[].invoiceID` | number |  |
| `paymentAllocations[].invoiceNumber` | number |  |
| `paymentAllocations[].paymentAllocationID` | number |  |
| `paymentAmount` | number |  |
| `paymentCategoryID` | object |  |
| `paymentCategoryName` | object |  |
| `paymentDate` | string |  |
| `paymentID` | number |  |
| `paymentNote` | object |  |
| `paymentReference` | object |  |
| `paymentType` | string |  |
| `propertyID` | number |  |
| `saleAmount` | number |  |
| `taxableAmount` | number |  |
| `taxAmount` | number |  |
| `taxJurisdictionID` | number |  |
| `taxJurisdictionName` | string |  |

## Native endpoint

Through the native Aspire API, this operation is `GET Payments` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payments.md) for the provider-specific parameters and requirements.

