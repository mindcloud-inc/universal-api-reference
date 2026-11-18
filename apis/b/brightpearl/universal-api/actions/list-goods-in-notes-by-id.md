# Brightpearl: List Goods-In Notes by ID



```
GET https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-goods-in-notes-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brightpearl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-goods-in-notes-by-id?connectionId=$CONNECTION_ID&orderIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-goods-in-notes-by-id?${params}`, {
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
| `orderIds` | string | yes | Order ID set, maximum 200 IDs. Use * only when supplying specific goods-in note IDs. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `goodsInNoteIds` | string | no | Optional goods-in note ID set, maximum 200 IDs. Required when Order IDs is *. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": 1,
      "goodsMoved": [
        {
          "allocated": true,
          "batchGoodsNoteId": 1,
          "cleared": true,
          "createdBy": 1,
          "createdOn": "2026-05-07T12:00:00.000Z",
          "destinationLocationId": 1,
          "goodsNoteId": 1,
          "productId": 1,
          "productValue": {
            "currency": "string",
            "value": "string"
          },
          "purchaseOrderRowId": 1,
          "quantity": 1,
          "quarantine": true,
          "updatedBy": 1,
          "updatedOn": "2026-05-07T12:00:00.000Z",
          "valueConfirmed": true,
          "warehouseId": 1
        }
      ],
      "goodsNoteId": 1,
      "goodsNoteStatus": "string",
      "id": 1,
      "orderId": 1,
      "receivedOn": "2026-05-07T12:00:00.000Z",
      "transfer": true,
      "userBatchReference": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | number |  |
| `goodsMoved` | array<object> |  |
| `goodsMoved[].allocated` | boolean |  |
| `goodsMoved[].batchGoodsNoteId` | number |  |
| `goodsMoved[].cleared` | boolean |  |
| `goodsMoved[].createdBy` | number |  |
| `goodsMoved[].createdOn` | date |  |
| `goodsMoved[].destinationLocationId` | number |  |
| `goodsMoved[].goodsNoteId` | number |  |
| `goodsMoved[].productId` | number |  |
| `goodsMoved[].productValue` | object |  |
| `goodsMoved[].productValue.currency` | string |  |
| `goodsMoved[].productValue.value` | string |  |
| `goodsMoved[].purchaseOrderRowId` | number |  |
| `goodsMoved[].quantity` | number |  |
| `goodsMoved[].quarantine` | boolean |  |
| `goodsMoved[].updatedBy` | number |  |
| `goodsMoved[].updatedOn` | date |  |
| `goodsMoved[].valueConfirmed` | boolean |  |
| `goodsMoved[].warehouseId` | number |  |
| `goodsNoteId` | number |  |
| `goodsNoteStatus` | string |  |
| `id` | number |  |
| `orderId` | number |  |
| `receivedOn` | date |  |
| `transfer` | boolean |  |
| `userBatchReference` | string |  |

## Native endpoint

Through the native Brightpearl API, this operation is `GET /warehouse-service/order/:orderIds/goods-note/goods-in/:goodsInNoteIds` (base URL `https://{{credentials.apiDomain}}/public-api/{{credentials.account}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-goods-in-notes-by-id.md) for the provider-specific parameters and requirements.

