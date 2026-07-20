# inFlow Inventory: List Stock Adjustments

Retrieves stock adjustments from inFlow Inventory.

```
GET https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/list-stock-adjustments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a inFlow Inventory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/list-stock-adjustments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/list-stock-adjustments?${params}`, {
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
      "adjustmentNumber": "string",
      "adjustmentReasonId": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "isCancelled": true,
      "lastModifiedById": "string",
      "locationId": "string",
      "remarks": "string",
      "stockAdjustmentId": "string",
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adjustmentNumber` | string |  |
| `adjustmentReasonId` | string |  |
| `date` | date |  |
| `isCancelled` | boolean |  |
| `lastModifiedById` | string |  |
| `locationId` | string |  |
| `remarks` | string |  |
| `stockAdjustmentId` | string |  |
| `timestamp` | string |  |

## Native endpoint

Through the native inFlow Inventory API, this operation is `GET /stock-adjustments` (base URL `https://cloudapi.inflowinventory.com/{{credentials.companyId}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-stock-adjustments.md) for the provider-specific parameters and requirements.

