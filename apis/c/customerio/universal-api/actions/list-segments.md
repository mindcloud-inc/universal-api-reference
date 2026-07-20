# Customer.io: List Segments

Retrieves segments from Customer.io.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-segments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-segments?${params}`, {
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
      "conditions": {},
      "createdAt": 1,
      "deduplicateId": "string",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "progress": 1,
      "state": "string",
      "tags": [
        "string"
      ],
      "type": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conditions` | object | The segment conditions object. |
| `createdAt` | number | The segment creation timestamp. |
| `deduplicateId` | string | The segment deduplication identifier. |
| `description` | string | The segment description. |
| `id` | number | The identifier for a segment. |
| `name` | string | The segment name. |
| `progress` | number | The segment processing progress. |
| `state` | string | The segment state. |
| `tags` | array<string> | The tags assigned to the segment. |
| `type` | string | The segment type. |
| `updatedAt` | number | The segment update timestamp. |

## Native endpoint

Through the native Customer.io API, this operation is `GET /v1/segments` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-segments.md) for the provider-specific parameters and requirements.

