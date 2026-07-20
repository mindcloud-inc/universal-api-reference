# inFlow Inventory: List Stock Transfers

Retrieves stock transfers from inFlow Inventory.

```
GET https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/list-stock-transfers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a inFlow Inventory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/list-stock-transfers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/list-stock-transfers?${params}`, {
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
      "assignedToTeamMemberId": "string",
      "fromLocationId": "string",
      "isCancelled": true,
      "lastModifiedById": "string",
      "receivedDate": "2026-05-07T12:00:00.000Z",
      "remarks": "string",
      "sentDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "stockTransferId": "string",
      "timestamp": "string",
      "toLocationId": "string",
      "transferDate": "2026-05-07T12:00:00.000Z",
      "transferNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedToTeamMemberId` | string |  |
| `fromLocationId` | string |  |
| `isCancelled` | boolean |  |
| `lastModifiedById` | string |  |
| `receivedDate` | date |  |
| `remarks` | string |  |
| `sentDate` | date |  |
| `status` | string |  |
| `stockTransferId` | string |  |
| `timestamp` | string |  |
| `toLocationId` | string |  |
| `transferDate` | date |  |
| `transferNumber` | string |  |

## Native endpoint

Through the native inFlow Inventory API, this operation is `GET /stock-transfers` (base URL `https://cloudapi.inflowinventory.com/{{credentials.companyId}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-stock-transfers.md) for the provider-specific parameters and requirements.

