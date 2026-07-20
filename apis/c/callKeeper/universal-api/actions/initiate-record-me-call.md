# CallKeeper: Initiate Record Me Call

Initiates a new record-me call in CallKeeper.

```
POST https://connect.mindcloud.co/v1/universal/callKeeper/latest/actions/initiate-record-me-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallKeeper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/callKeeper/latest/actions/initiate-record-me-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callKeeper/latest/actions/initiate-record-me-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "items": [
        {}
      ],
      "message": "string",
      "page": 1,
      "page_size": 1,
      "status": "string",
      "total": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Creation timestamp. |
| `id` | string | Resource identifier. |
| `items` | array<object> | Returned collection items. |
| `message` | string | Status or result message. |
| `page` | number | Current page number. |
| `page_size` | number | Page size. |
| `status` | string | Resource or operation status. |
| `total` | number | Total result count. |
| `updated_at` | date | Last update timestamp. |
| `url` | string | Returned URL when available. |

## Native endpoint

Through the native CallKeeper API, this operation is `POST /calls/record-me` (base URL `https://api.callkeeper.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initiate-record-me-call.md) for the provider-specific parameters and requirements.

