# Brightpearl: List Goods-In Notes



```
GET https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-goods-in-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brightpearl `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-goods-in-notes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-goods-in-notes?${params}`, {
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
      "batchId": 1,
      "createdDate": "2026-05-07T12:00:00.000Z",
      "currCode": "string",
      "groupingA": "string",
      "groupingB": "string",
      "groupingC": "string",
      "groupingD": "string",
      "landedCosts": "string",
      "locationId": 1,
      "onHand": 1,
      "price": "string",
      "productId": 1,
      "purchaseOrderId": 1,
      "receivedDate": "2026-05-07T12:00:00.000Z",
      "receivedQuantity": 1,
      "userBatchRef": "string",
      "warehouseId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchId` | number | Id of the batch which the stock was received on. |
| `createdDate` | date |  |
| `currCode` | string | Currency for value. |
| `groupingA` | string |  |
| `groupingB` | string |  |
| `groupingC` | string |  |
| `groupingD` | string |  |
| `landedCosts` | string | The landed costs for the stock. |
| `locationId` | number | The location ID of the stock. |
| `onHand` | number | The quantity on hand for this batch in this location at this price for the product. |
| `price` | string | The value for the stock. |
| `productId` | number | The product Id. |
| `purchaseOrderId` | number | The ID of the purchase order. |
| `receivedDate` | date |  |
| `receivedQuantity` | number | The quantity recieved as part of this batch into location for given price. |
| `userBatchRef` | string | User supplied reference for the batch. |
| `warehouseId` | number | The warehouse Id. |

## Native endpoint

Through the native Brightpearl API, this operation is `GET /warehouse-service/goods-in-search` (base URL `https://{{credentials.apiDomain}}/public-api/{{credentials.account}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-goods-in-notes.md) for the provider-specific parameters and requirements.

