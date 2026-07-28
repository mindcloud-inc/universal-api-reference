# Ramp: List Transactions



```
GET https://connect.mindcloud.co/v1/universal/ramp/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ramp `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ramp/latest/actions/list-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ramp/latest/actions/list-transactions?${params}`, {
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
| `accountingFieldSelectionId` | string | no |  |
| `approvalStatus` | string | no |  |
| `awaitingApprovalByUserId` | string | no |  |
| `cardId` | string | no |  |
| `departmentId` | string | no |  |
| `entityId` | string | no |  |
| `fromDate` | string | no |  |
| `hasNoSyncCommits` | boolean | no |  |
| `includeMerchantData` | boolean | no |  |
| `limitId` | string | no |  |
| `locationId` | string | no |  |
| `maxAmount` | number | no |  |
| `merchantId` | string | no |  |
| `minAmount` | number | no |  |
| `orderByAmountAsc` | boolean | no |  |
| `orderByAmountDesc` | boolean | no |  |
| `orderByDateAsc` | boolean | no |  |
| `orderByDateDesc` | boolean | no |  |
| `requiresMemo` | boolean | no |  |
| `skCategoryId` | string | no |  |
| `spendProgramId` | string | no |  |
| `state` | string | no |  |
| `statementId` | string | no |  |
| `syncedAfter` | string | no |  |
| `syncReady` | boolean | no |  |
| `syncStatus` | string | no |  |
| `toDate` | string | no |  |
| `tripId` | string | no |  |
| `userId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ramp API returns.

## Native endpoint

Through the native Ramp API, this operation is `GET transactions` (base URL `https://api.ramp.com/developer/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

