# Inoreader: List Stream Item IDs

Retrieves item IDs from an Inoreader stream.

```
GET https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/list-stream-item-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Inoreader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/list-stream-item-ids?connectionId=$CONNECTION_ID&streamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "streamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/list-stream-item-ids?${params}`, {
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
| `streamId` | string | yes | Stream ID to fetch item IDs from. |
| `maxItems` | number | no | Number of item IDs to return. |
| `order` | string | no | Return newest first by default, or oldest first with o. |
| `startTime` | number | no | Unix timestamp from which to begin fetching item IDs. |
| `excludeTarget` | string | no | Exclude a target stream or state such as the read state. |
| `includeTarget` | string | no | Include only item IDs matching a specific target label or state. |
| `continuation` | string | no | Continuation token from a previous response. |
| `includeAllDirectStreamIds` | boolean | no | Include automatically added folder tags in direct stream IDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "continuation": "string",
      "direction": "string",
      "itemRefs": [
        {}
      ],
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `continuation` | string | Continuation token for the next page when more item IDs are available. |
| `direction` | string | Detected text direction if present in the response. |
| `itemRefs` | array<object> | Article ID references with direct stream IDs and timestamps. |
| `items` | array<object> | Lightweight list placeholder returned by the endpoint. |

## Native endpoint

Through the native Inoreader API, this operation is `GET /stream/items/ids` (base URL `https://www.inoreader.com/reader/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stream-item-ids.md) for the provider-specific parameters and requirements.

