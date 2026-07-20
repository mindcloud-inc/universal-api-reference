# Aspire: List Revenue Variances

Retrieves revenue variances from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-revenue-variances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-revenue-variances?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-revenue-variances?${params}`, {
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
      "AccountingPeriodID": 1,
      "Adjustment": 1,
      "AdjustmentDate": "2026-05-07T12:00:00.000Z",
      "BranchID": 1,
      "BranchName": "Ava Chen",
      "ContractYear": 1,
      "CreatedByUserID": 1,
      "CreatedByUserName": "Ava Chen",
      "CreatedDateTime": "2026-05-07T12:00:00.000Z",
      "DivisionID": 1,
      "DivisionName": "Ava Chen",
      "EarnedRevenue": 1,
      "InvoiceRevenue": 1,
      "OpportunityID": 1,
      "OpportunityNumber": 1,
      "RevenueVarianceID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AccountingPeriodID` | number |  |
| `Adjustment` | number |  |
| `AdjustmentDate` | date |  |
| `BranchID` | number |  |
| `BranchName` | string |  |
| `ContractYear` | number |  |
| `CreatedByUserID` | number |  |
| `CreatedByUserName` | string |  |
| `CreatedDateTime` | date |  |
| `DivisionID` | number |  |
| `DivisionName` | string |  |
| `EarnedRevenue` | number |  |
| `InvoiceRevenue` | number |  |
| `OpportunityID` | number |  |
| `OpportunityNumber` | number |  |
| `RevenueVarianceID` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `GET RevenueVariances` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-revenue-variances.md) for the provider-specific parameters and requirements.

