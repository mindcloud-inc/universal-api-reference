# Aspire: List Invoice Batches

Retrieves invoice batches from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-invoice-batches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-invoice-batches?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-invoice-batches?${params}`, {
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
      "accountingPeriodID": {},
      "accountingPeriodName": {},
      "createdByUserID": 1,
      "createdByUserName": "Ava Chen",
      "createdDateTime": "string",
      "customerEventDescription": {},
      "customerEventEndDateTime": {},
      "customerEventID": {},
      "customerEventName": {},
      "customerEventStartDateTime": {},
      "customerEventTypeID": {},
      "customerEventTypeName": {},
      "invoiceBatchID": 1,
      "invoiceBatchNumber": 1,
      "invoiceBatchStatus": "string",
      "submitDateTime": "string",
      "submittedByUserID": 1,
      "submittedByUserName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountingPeriodID` | object |  |
| `accountingPeriodName` | object |  |
| `createdByUserID` | number |  |
| `createdByUserName` | string |  |
| `createdDateTime` | string |  |
| `customerEventDescription` | object |  |
| `customerEventEndDateTime` | object |  |
| `customerEventID` | object |  |
| `customerEventName` | object |  |
| `customerEventStartDateTime` | object |  |
| `customerEventTypeID` | object |  |
| `customerEventTypeName` | object |  |
| `invoiceBatchID` | number |  |
| `invoiceBatchNumber` | number |  |
| `invoiceBatchStatus` | string |  |
| `submitDateTime` | string |  |
| `submittedByUserID` | number |  |
| `submittedByUserName` | string |  |

## Native endpoint

Through the native Aspire API, this operation is `GET InvoiceBatches` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoice-batches.md) for the provider-specific parameters and requirements.

