# Sage Intacct: Create Bill Item



```
POST https://connect.mindcloud.co/v1/universal/intacct/latest/actions/createbillitem
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sage Intacct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/createbillitem" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intacct/latest/actions/createbillitem', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apbillitems[].accountNo` | string | no |  |
| `apbillitems[].taxEntries[].detailId` | string | no |  |
| `whenCreated` | string | no |  |
| `apbillitems[].accountLabel` | string | no |  |
| `apbillitems[].taxEntries[].trx_tax` | string | no |  |
| `whenPosted` | string | no |  |
| `apbillitems[].offsetGlaAccountNo` | string | no |  |
| `vendorId` | string | no |  |
| `apbillitems[].trxAmount` | string | no |  |
| `recordId` | string | no |  |
| `apbillitems[].totalTrxAmount` | string | no |  |
| `docNumber` | string | no |  |
| `apbillitems[].entryDescription` | string | no |  |
| `description` | string | no |  |
| `apbillitems[].form1099` | boolean | no |  |
| `termName` | string | no |  |
| `apbillitems[].form1099Type` | string | no |  |
| `recPaymentDate` | string | no |  |
| `apbillitems[].form1099Box` | string | no |  |
| `supdocid` | string | no |  |
| `apbillitems[].billable` | boolean | no |  |
| `whenDue` | string | no |  |
| `apbillitems[].allocationId` | string | no |  |
| `paymentPriority` | string | no |  |
| `apbillitems[].departmentId` | string | no |  |
| `onHold` | boolean | no |  |
| `apbillitems[].projectId` | string | no |  |
| `currency` | string | no |  |
| `apbillitems[].taskId` | string | no |  |
| `baseCurr` | string | no |  |
| `apbillitems[]` | array | no |  |
| `apbillitems[].costTypeId` | string | no |  |
| `apbillitems[].customerId` | string | no |  |
| `apbillitems[].customerId` | string | no |  |
| `apbillitems[].vendorId` | string | no |  |
| `apbillitems[].employeeId` | string | no |  |
| `apbillitems[].itemId` | string | no |  |
| `apbillitems[].classId` | string | no |  |
| `apbillitems[].contractId` | string | no |  |
| `apbillitems[].warehouseId` | string | no |  |
| `apbillitems[].gldim*` | number | no |  |
| `apbillitems[].partialExempt` | boolean | no |  |
| `apbillitems[].taxEntries[]` | array | no |  |
| `apbillitems[].locationId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sage Intacct API returns.

## Native endpoint

Through the native Sage Intacct API, this operation is `POST` (base URL `https://api.intacct.com/ia/xml/xmlgw.phtml`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/createbillitem.md) for the provider-specific parameters and requirements.

