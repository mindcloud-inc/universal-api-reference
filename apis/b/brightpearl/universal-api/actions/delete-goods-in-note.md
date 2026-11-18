# Brightpearl: Delete Goods-In Note



```
DELETE https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/delete-goods-in-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brightpearl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/delete-goods-in-note?connectionId=$CONNECTION_ID&goodsInNoteId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "goodsInNoteId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/delete-goods-in-note?${params}`, {
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
| `goodsInNoteId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Brightpearl API returns.

## Native endpoint

Through the native Brightpearl API, this operation is `DELETE /warehouse-service/goods-note/goods-in/:goodsInNoteId` (base URL `https://{{credentials.apiDomain}}/public-api/{{credentials.account}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-goods-in-note.md) for the provider-specific parameters and requirements.

