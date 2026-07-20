# EasyPost: List Trackers

Retrieves a list of trackers from EasyPost.

```
GET https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/list-trackers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/list-trackers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/list-trackers?${params}`, {
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
      "carrier": "string",
      "id": "string",
      "mode": "string",
      "object": "string",
      "publicUrl": "https://example.com",
      "status": "string",
      "statusDetail": "string",
      "trackingCode": "string",
      "trackingDetails": [
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
| `carrier` | string |  |
| `id` | string |  |
| `mode` | string |  |
| `object` | string |  |
| `publicUrl` | string |  |
| `status` | string |  |
| `statusDetail` | string |  |
| `trackingCode` | string |  |
| `trackingDetails` | array<object> |  |

## Native endpoint

Through the native EasyPost API, this operation is `GET /trackers` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-trackers.md) for the provider-specific parameters and requirements.

