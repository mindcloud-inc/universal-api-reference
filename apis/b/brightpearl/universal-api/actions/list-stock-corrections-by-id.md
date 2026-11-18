# Brightpearl: List Stock Corrections by ID



```
GET https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-stock-corrections-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brightpearl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-stock-corrections-by-id?connectionId=$CONNECTION_ID&warehouseId=1&stockCorrectionIds=100-120%2C130" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "warehouseId": "1",
  "stockCorrectionIds": "100-120,130"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-stock-corrections-by-id?${params}`, {
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
| `warehouseId` | number | yes |  |
| `stockCorrectionIds` | string | yes | A single ID, comma-separated IDs, or ranges. Maximum 200 IDs. Example: `100-120,130`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "goodsMoved": [
        {
          "batchGoodsNoteId": 1,
          "createdBy": 1,
          "createdOn": "2026-05-07T12:00:00.000Z",
          "destinationLocationId": 1,
          "productId": 1,
          "productValue": {
            "currency": "string",
            "value": 1
          },
          "quantity": 1
        }
      ],
      "goodsNoteId": 1,
      "reason": "string",
      "warehouseId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `goodsMoved` | array<object> |  |
| `goodsMoved[].batchGoodsNoteId` | number |  |
| `goodsMoved[].createdBy` | number |  |
| `goodsMoved[].createdOn` | date |  |
| `goodsMoved[].destinationLocationId` | number |  |
| `goodsMoved[].productId` | number |  |
| `goodsMoved[].productValue` | object |  |
| `goodsMoved[].productValue.currency` | string |  |
| `goodsMoved[].productValue.value` | number |  |
| `goodsMoved[].quantity` | number |  |
| `goodsNoteId` | number |  |
| `reason` | string |  |
| `warehouseId` | number |  |

## Native endpoint

Through the native Brightpearl API, this operation is `GET /warehouse-service/warehouse/:warehouseId/stock-correction/:stockCorrectionIds` (base URL `https://{{credentials.apiDomain}}/public-api/{{credentials.account}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stock-corrections-by-id.md) for the provider-specific parameters and requirements.

