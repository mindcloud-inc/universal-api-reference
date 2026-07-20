# WaniKani: List Review Statistics

Retrieves review statistics from WaniKani.

```
GET https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/list-review-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaniKani `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/list-review-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/list-review-statistics?${params}`, {
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
      "data": {},
      "dataUpdatedAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "object": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `dataUpdatedAt` | date |  |
| `id` | number |  |
| `object` | string |  |
| `url` | string |  |

## Native endpoint

Through the native WaniKani API, this operation is `GET /review_statistics` (base URL `https://api.wanikani.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-review-statistics.md) for the provider-specific parameters and requirements.

