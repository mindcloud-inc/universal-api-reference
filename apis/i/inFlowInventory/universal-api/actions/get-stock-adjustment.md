# inFlow Inventory: Get Stock Adjustment

Retrieves an existing stock adjustment from inFlow Inventory.

```
GET https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-stock-adjustment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a inFlow Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-stock-adjustment?connectionId=$CONNECTION_ID&stockAdjustmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stockAdjustmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-stock-adjustment?${params}`, {
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
| `stockAdjustmentId` | string | yes | The unique identifier of the stock adjustment to retrieve. |

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

Through the native inFlow Inventory API, this operation is `GET /stock-adjustments/:stockAdjustmentId` (base URL `https://cloudapi.inflowinventory.com/{{credentials.companyId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stock-adjustment.md) for the provider-specific parameters and requirements.

