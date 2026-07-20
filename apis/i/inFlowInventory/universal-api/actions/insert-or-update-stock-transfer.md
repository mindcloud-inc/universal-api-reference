# inFlow Inventory: Insert or Update Stock Transfer

Inserts or updates a stock transfer in inFlow Inventory.

```
PUT https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/insert-or-update-stock-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a inFlow Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/insert-or-update-stock-transfer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/insert-or-update-stock-transfer', {
  method: 'PUT',
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

Through the native inFlow Inventory API, this operation is `PUT /stock-transfers` (base URL `https://cloudapi.inflowinventory.com/{{credentials.companyId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-or-update-stock-transfer.md) for the provider-specific parameters and requirements.

