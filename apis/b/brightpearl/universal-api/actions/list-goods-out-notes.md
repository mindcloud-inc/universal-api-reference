# Brightpearl: List Goods-Out Notes



```
GET https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-goods-out-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brightpearl `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-goods-out-notes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-goods-out-notes?${params}`, {
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
      "channelId": 1,
      "createdBy": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "goodsOutNoteId": 1,
      "labelUri": "string",
      "orderId": 1,
      "packed": true,
      "picked": true,
      "printed": true,
      "priority": true,
      "releaseDate": "2026-05-07T12:00:00.000Z",
      "shipped": true,
      "shippedOn": "2026-05-07T12:00:00.000Z",
      "shippingMethodId": 1,
      "transfer": true,
      "warehouseId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelId` | number | The Channel ID for the related order |
| `createdBy` | number | The ID of the contact that created this goods out note. |
| `createdOn` | date | The date the goods out note was created on. |
| `goodsOutNoteId` | number | The ID of the goods out note. |
| `labelUri` | string | The URL of the shipping label image (optional) |
| `orderId` | number | The ID of the order for the goods out note. Can be used to recover information about an order with an Order GET |
| `packed` | boolean | Details whether a goods out note has been packed. |
| `picked` | boolean | Details whether a goods out note has been printed. |
| `printed` | boolean | Details whether a goods out note has been printed. |
| `priority` | boolean | The priority of the goods out note. |
| `releaseDate` | date | The date the goods out note is to be released. |
| `shipped` | boolean | Details whether a goods out note has been shipped. |
| `shippedOn` | date | The date the goods out note was shipped on. |
| `shippingMethodId` | number |  |
| `transfer` | boolean | Details whether a goods out note is a transfer. |
| `warehouseId` | number | The ID of the warehouse for the goods out note. Can be used to recover information about a warehouse with a Warehouse GET |

## Native endpoint

Through the native Brightpearl API, this operation is `GET /warehouse-service/goods-note/goods-out-search` (base URL `https://{{credentials.apiDomain}}/public-api/{{credentials.account}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-goods-out-notes.md) for the provider-specific parameters and requirements.

