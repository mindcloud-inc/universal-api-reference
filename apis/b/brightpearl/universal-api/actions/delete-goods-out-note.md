# Brightpearl: Delete Goods-Out Note



```
DELETE https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/delete-goods-out-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brightpearl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/delete-goods-out-note?connectionId=$CONNECTION_ID&orderId=1&goodsOutNoteId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "1",
  "goodsOutNoteId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/delete-goods-out-note?${params}`, {
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
| `orderId` | number | yes |  |
| `goodsOutNoteId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Brightpearl API, this operation is `DELETE /warehouse-service/order/:orderId/goods-note/goods-out/:goodsOutNoteId` (base URL `https://{{credentials.apiDomain}}/public-api/{{credentials.account}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-goods-out-note.md) for the provider-specific parameters and requirements.

