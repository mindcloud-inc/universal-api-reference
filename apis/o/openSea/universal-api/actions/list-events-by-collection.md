# OpenSea: Get Events By Collection

Retrieves events for an OpenSea collection.

```
GET https://connect.mindcloud.co/v1/universal/openSea/latest/actions/list-events-by-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSea `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSea/latest/actions/list-events-by-collection?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSea/latest/actions/list-events-by-collection?${params}`, {
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
| `slug` | string | yes | Unique identifier for the collection |
| `after` | number | no | Only show events after this timestamp (Unix timestamp in seconds) |
| `before` | number | no | Only show events before this timestamp (Unix timestamp in seconds) |
| `eventType[]` | array<string> | no | Filter by event types. To get order invalidation and revalidation events, please use the Stream API. The order status can also be checked on the Get Order endpoint. Accepts multiple values in one string, delimited by `,`. |
| `limit` | number | no | Number of items to return per page |
| `nextValue` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |

## Native endpoint

Through the native OpenSea API, this operation is `GET /api/v2/events/collection/{slug}` (base URL `https://api.opensea.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events-by-collection.md) for the provider-specific parameters and requirements.

