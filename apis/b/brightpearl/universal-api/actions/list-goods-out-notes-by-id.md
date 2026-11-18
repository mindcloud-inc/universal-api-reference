# Brightpearl: List Goods-Out Notes by ID



```
GET https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-goods-out-notes-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brightpearl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-goods-out-notes-by-id?connectionId=$CONNECTION_ID&orderIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-goods-out-notes-by-id?${params}`, {
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
| `orderIds` | string | yes | Order ID set, maximum 500 IDs. Use * only when supplying specific goods-out note IDs. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `goodsOutNoteIds` | string | no | Optional goods-out note ID set, maximum 500 IDs. Required when Order IDs is *. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "events": [
        {
          "eventCode": "string",
          "eventOwnerId": 1,
          "occured": "2026-05-07T12:00:00.000Z"
        }
      ],
      "id": 1,
      "labelUri": "string",
      "lastEventVersion": 1,
      "orderId": 1,
      "orderRows": {},
      "priority": true,
      "releaseDate": "2026-05-07T12:00:00.000Z",
      "sequence": 1,
      "shipping": {
        "boxes": 1,
        "reference": "string",
        "shippingMethodId": 1,
        "weight": "string"
      },
      "status": {
        "packed": true,
        "packedById": 1,
        "packedOn": "2026-05-07T12:00:00.000Z",
        "picked": true,
        "pickedById": 1,
        "pickedOn": "2026-05-07T12:00:00.000Z",
        "printed": true,
        "printedById": 1,
        "printedOn": "2026-05-07T12:00:00.000Z",
        "shipped": true,
        "shippedById": 1,
        "shippedOn": "2026-05-07T12:00:00.000Z"
      },
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
| `createdBy` | number |  |
| `createdOn` | date |  |
| `events` | array<object> |  |
| `events[].eventCode` | string |  |
| `events[].eventOwnerId` | number |  |
| `events[].occured` | date |  |
| `id` | number |  |
| `labelUri` | string |  |
| `lastEventVersion` | number |  |
| `orderId` | number |  |
| `orderRows` | object |  |
| `priority` | boolean |  |
| `releaseDate` | date |  |
| `sequence` | number |  |
| `shipping` | object |  |
| `shipping.boxes` | number |  |
| `shipping.reference` | string |  |
| `shipping.shippingMethodId` | number |  |
| `shipping.weight` | string |  |
| `status` | object |  |
| `status.packed` | boolean |  |
| `status.packedById` | number |  |
| `status.packedOn` | date |  |
| `status.picked` | boolean |  |
| `status.pickedById` | number |  |
| `status.pickedOn` | date |  |
| `status.printed` | boolean |  |
| `status.printedById` | number |  |
| `status.printedOn` | date |  |
| `status.shipped` | boolean |  |
| `status.shippedById` | number |  |
| `status.shippedOn` | date |  |
| `transfer` | boolean |  |
| `warehouseId` | number |  |

## Native endpoint

Through the native Brightpearl API, this operation is `GET /warehouse-service/order/:orderIds/goods-note/goods-out/:goodsOutNoteIds` (base URL `https://{{credentials.apiDomain}}/public-api/{{credentials.account}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-goods-out-notes-by-id.md) for the provider-specific parameters and requirements.

