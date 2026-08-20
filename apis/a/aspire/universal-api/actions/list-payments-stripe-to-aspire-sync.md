# Aspire: List Payments – Stripe to Aspire Sync



```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-payments-stripe-to-aspire-sync
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-payments-stripe-to-aspire-sync?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-payments-stripe-to-aspire-sync?${params}`, {
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
      "bankDepositID": 1,
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
      "electronicPaymentID": 1,
      "emailStatus": "ava@example.com",
      "isExpense": true,
      "lastModifiedByUserID": 1,
      "lastModifiedByUserName": "Ava Chen",
      "lastModifiedDateTime": "string",
      "opportunityID": 1,
      "paymentAmount": 1,
      "paymentCategoryID": 1,
      "paymentCategoryName": "Ava Chen",
      "paymentDate": "string",
      "paymentID": 1,
      "paymentNote": "string",
      "paymentReference": "string",
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
| `bankDepositID` | number | Aspire Payments response field. |
| `billingAddressID` | number | Aspire Payments response field. |
| `branchID` | number | Aspire Payments response field. |
| `branchName` | string | Aspire Payments response field. |
| `companyID` | number | Aspire Payments response field. |
| `companyName` | string | Aspire Payments response field. |
| `contactID` | number | Aspire Payments response field. |
| `contactName` | string | Aspire Payments response field. |
| `createdByUserID` | number | Aspire Payments response field. |
| `createdByUserName` | string | Aspire Payments response field. |
| `createdDateTime` | string | Aspire Payments response field. |
| `creditMemoNumber` | number | Aspire Payments response field. |
| `divisionID` | number | Aspire Payments response field. |
| `divisionName` | string | Aspire Payments response field. |
| `electronicPaymentID` | number | Aspire Payments response field. |
| `emailStatus` | string | Aspire Payments response field. |
| `isExpense` | boolean | Aspire Payments response field. |
| `lastModifiedByUserID` | number | Aspire Payments response field. |
| `lastModifiedByUserName` | string | Aspire Payments response field. |
| `lastModifiedDateTime` | string | Aspire Payments response field. |
| `opportunityID` | number | Aspire Payments response field. |
| `paymentAmount` | number | Aspire Payments response field. |
| `paymentCategoryID` | number | Aspire Payments response field. |
| `paymentCategoryName` | string | Aspire Payments response field. |
| `paymentDate` | string | Aspire Payments response field. |
| `paymentID` | number | Aspire Payments response field. |
| `paymentNote` | string | Aspire Payments response field. |
| `paymentReference` | string | Aspire Payments response field. |
| `paymentType` | string | Aspire Payments response field. |
| `propertyID` | number | Aspire Payments response field. |
| `saleAmount` | number | Aspire Payments response field. |
| `taxableAmount` | number | Aspire Payments response field. |
| `taxAmount` | number | Aspire Payments response field. |
| `taxJurisdictionID` | number | Aspire Payments response field. |
| `taxJurisdictionName` | string | Aspire Payments response field. |

## Native endpoint

Through the native Aspire API, this operation is `GET Payments` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payments-stripe-to-aspire-sync.md) for the provider-specific parameters and requirements.

