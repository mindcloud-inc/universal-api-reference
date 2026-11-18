# Brightpearl: Update Goods-Out Note



```
PUT https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/update-goods-out-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brightpearl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/update-goods-out-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "goodsOutNoteId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/update-goods-out-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "goodsOutNoteId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `goodsOutNoteId` | number | yes |  |
| `priority` | boolean | no |  |
| `shipping` | object | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shipping.shippingMethodId` | number | no |  |
| `shipping.reference` | string | no |  |
| `shipping.boxes` | number | no |  |
| `shipping.weight` | string | no | Total weight, at most 999999.99. |
| `labelUri` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Brightpearl API returns.

## Native endpoint

Through the native Brightpearl API, this operation is `PUT /warehouse-service/goods-note/goods-out/:goodsOutNoteId` (base URL `https://{{credentials.apiDomain}}/public-api/{{credentials.account}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-goods-out-note.md) for the provider-specific parameters and requirements.

